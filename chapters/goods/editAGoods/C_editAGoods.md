```javascript
const path=require('path');
const fs=require('fs');
const pump = require('mz-modules/pump');

const Controller = require('egg').Controller;

class GoodsController extends Controller {
  async getEditForm() { const { ctx } = this;      
    let goodsId = ctx.params.id;
    const goods = await ctx.model.Goods.find({_id: goodsId});
    await ctx.render('goods/edit.tpl', {goods: goods[0], title:'编辑商品'});
  };

  async editGoodsData() { const { ctx } = this;      
    let goodsId = ctx.params.id;

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

    await ctx.model.Goods.findOneAndUpdate({_id: goodsId}, {
                                        ...parts.field,     // grammar sugar                                  
                                       "createdAt": new Date(),
                                     });
    ctx.redirect("/admin/goods/adminShowAll");          
  };

}

module.exports = GoodsController; 
```


