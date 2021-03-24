```javascript
const Controller = require('egg').Controller;

class OrderController extends Controller {

  async getCreateForm() { const { ctx } = this;
    await ctx.render("order/create.tpl",{title:'成为会员'});
  };

  async insertOrderData() { const { ctx } = this;
    ctx.body = '<h1>first, need to pay to alipay</h1>'

  }
}

module.exports = OrderController;
```


