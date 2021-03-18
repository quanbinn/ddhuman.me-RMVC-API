```javascript
const Controller = require('egg').Controller;

class HomeController extends Controller {
  
  async index() { const { ctx } = this;
    // console.log(ctx.session);
    // console.log(ctx.session.role);
    // console.log(ctx.session.role == null);
    await ctx.render('homeAnd6Categories/home.tpl', {title:'首页'});
  }

}

module.exports = HomeController;
```

