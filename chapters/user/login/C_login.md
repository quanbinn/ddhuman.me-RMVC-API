```javascript
const Controller = require('egg').Controller;

class UserController extends Controller {
  async getLoginForm() { const { ctx } = this;
    await ctx.render("user/login.tpl",{title:'登录'});
  };

  async checkUserData() { const { ctx } = this;
    // console.log(ctx.request.body);
    let username = ctx.request.body.username;
	  let password = this.service.tools.md5(ctx.request.body.password);

	  // save into session in memory
    ctx.session.username = username;
    ctx.session.password = password;	

	const userInDatabase = await ctx.model.User.find({username: username});

  	if (userInDatabase.length == 0 ) {
  		ctx.body = "<h1>用户名错误，请重新</h1><h1><a href='/user/registerForm'>注册</a>	或	<a href='/user/loginForm'>登录</a></h1><link rel='stylesheet' type='text/css' href='/public/css/style.css'>";
  	} else if (ctx.session.password == userInDatabase[0]["password"]) {
      ctx.session.role = userInDatabase[0]["role"];    
      console.log(ctx.session.role);      
  		if (userInDatabase[0]["role"] == "管理员") {
  			ctx.redirect('/admin');
  		} else if (userInDatabase[0]["role"] == "付费用户") {
  			ctx.redirect('/speedyShopping/learnEquip');
  		} else {
  			ctx.redirect('/');
  		} 
  	} else {
  		ctx.body = "<h1>密码错误，请重新输入</h1><h1><a href='/user/loginForm'>登录</a></h1><link rel='stylesheet' type='text/css' href='/public/css/style.css'</h1>";
  	}
  }

}

module.exports = UserController;
```

