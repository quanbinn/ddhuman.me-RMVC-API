```javascript
const Controller = require('egg').Controller;

class ExperimentController extends Controller {

  async show() { const { ctx } = this;      
    let expId = ctx.params.id;
    const experiment = await ctx.model.Experiment.find({_id: expId});

    console.log(ctx.session.role);
    
  	if (ctx.session.role == null) {
  		ctx.body = "<h1>观看内容，您需要</h1><h1><a href='/user/registerForm'>注册</a>	或	<a href='/user/loginForm'>登录</a></h1><link rel='stylesheet' type='text/css' href='/public/css/style.css'>";
  	} else {
  		await ctx.render('experiment/show.tpl', {exp: experiment[0],title:'显示实验'});
  	}
  };

}

module.exports = ExperimentsController;
```


