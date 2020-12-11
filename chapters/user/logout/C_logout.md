```javascript
const Controller = require("egg").Controller;

class LogoutController extends Controller {
  async removePermission() {
    const { ctx } = this;
    // console.log(ctx.request.body);
    // let username = ctx.request.body.username;
    // let password = ctx.request.body.password;
    // check user data
    // await ctx.model.User.create({"username": username, "password": password});
    // ctx.body = "登录成功"
  }
}

module.exports = LogoutController;
```

