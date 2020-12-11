```javascript
const Controller = require("egg").Controller;

class LoginController extends Controller {
  async getForm() { 
    const { ctx } = this;
    await ctx.render("user/login.tpl");
  };

  async checkUserData() {
    const { ctx } = this;
    // console.log(ctx.request.body);
    let username = ctx.request.body.username;
    let password = ctx.request.body.password;
    // check user data
    // await ctx.model.User.create({"username": username, "password": password});
    // ctx.body = "登录成功"
  }
}

module.exports = LoginController;
```

