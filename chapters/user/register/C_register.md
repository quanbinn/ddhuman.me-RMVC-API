```javascript
const Controller = require('egg').Controller;

class UserController extends Controller {

  async getRegisterForm() { const { ctx } = this;
    await ctx.render("user/register.tpl",{title:'注册'});
  };

  async insertUserData() { const { ctx } = this;
    // console.log(ctx.request.body);
    let username = ctx.request.body.username;
    let password = this.service.tools.md5(ctx.request.body.password);

    const userInDatabase = await ctx.model.User.find({username: username});    
    // console.log(userInDatabase,'asssss');

    if (userInDatabase.length == 1) {
  	  ctx.body = "<h1>用户名已经存在，请输入一个新的用户名</h1><h1><a href='/user/registerForm'>注册</a></h1><link rel='stylesheet' type='text/css' href='/public/css/style.css'>";
    } else {
        await ctx.model.User.create({
                               "username": username, 
                                "password": password,
                                "role": "普通用户", 
                                "createdAt": new Date()
                            });

        ctx.session.username = username;
        ctx.session.password = password;
		ctx.session.role = '普通用户';
        ctx.redirect("/");  
    }
  }

}

module.exports = UserController;
```


