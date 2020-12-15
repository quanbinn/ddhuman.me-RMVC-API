```javascript
const Controller = require("egg").Controller;

class RegisterController extends Controller {
  async getForm() { 
    const { ctx } = this;
    await ctx.render("user/register.tpl");
  };

  async insertUserData() {
    const { ctx } = this;
    // console.log(ctx.request.body);
    let username = ctx.request.body.username;
    let password = ctx.request.body.password;
    await ctx.model.User.create({"username": username, "password": password});
    ctx.body = "注册成功"
  }
}

module.exports = RegisterController;
```


