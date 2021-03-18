```javascript
const Controller = require('egg').Controller;

class UserController extends Controller {
  async logout() { const { ctx } = this;  
      ctx.session.username = null;
      ctx.session.password = null;    
      ctx.session.role = null;

      await ctx.redirect("/"); 
  }

}

module.exports = UserController;
```

