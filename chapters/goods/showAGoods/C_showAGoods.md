```javascript
const Controller = require('egg').Controller;

class GoodsController extends Controller {

  async show() { const { ctx } = this;      
    let goodsId = ctx.params.id;
    const goods = await ctx.model.Goods.find({_id: goodsId});
    await ctx.render('goods/show.tpl', {goods: goods[0], title:'显示商品'});
  };

}

module.exports = GoodsController; 
```


