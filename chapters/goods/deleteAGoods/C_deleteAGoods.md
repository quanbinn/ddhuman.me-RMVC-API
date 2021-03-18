```javascript
const Controller = require('egg').Controller;

class GoodsController extends Controller {

  async removeGoodsData() { const { ctx } = this;      
    let goodsId = ctx.params.id;
    await ctx.model.Goods.deleteOne({_id: goodsId});
    ctx.redirect("/admin/goods/adminShowAll");      
  };  

}

module.exports = GoodsController; 
```


