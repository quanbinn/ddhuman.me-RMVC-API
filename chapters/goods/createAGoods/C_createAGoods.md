```javascript
const path=require('path');
const fs=require('fs');
const pump = require('mz-modules/pump');

const Controller = require('egg').Controller;

class GoodsController extends Controller {
  async getCreateForm() { const { ctx } = this; 
  	await ctx.render("goods/create.tpl", {title:'创建新商品'});
  };

  async insertGoodsData() { const { ctx } = this;
    const parts = ctx.multipart({ autoFields: true });

    let stream;
    while ((stream = await parts()) != null) {
        if (!stream.filename) { 
          return;
        }       

        const target = 'app/public/upload/'+parts.field['category']+'/'+parts.field['subcategory']+'/'+parts.field['goodsname']+'/'+path.basename(stream.filename);
        parts.field[stream.fieldname] = target.replace("app","");         

        const writeStream = fs.createWriteStream(target);
        await pump(stream, writeStream);  
    };

    delete parts.field["_csrf"];       //let {} = parts.field;

    await ctx.model.Goods.create({
                                        ...parts.field,     // grammar sugar
                                       "createdAt": new Date(),
                                     });
    ctx.body = "创建新商品成功";         
  };

}

module.exports = GoodsController; 
```


