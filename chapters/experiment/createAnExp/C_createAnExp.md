```javascript
const Controller = require('egg').Controller;

class ExperimentController extends Controller {
  async getForm() { 
    const { ctx } = this;
    await ctx.render("experiment/create.tpl");
  };
    
  async insertExpData() {
    const { ctx } = this;
    let title = ctx.request.body.title;
    let showImage = ctx.request.body.showImage;    
    let url = ctx.request.body.url;
    let category = ctx.request.body.category;         
	// later add userId  
    await ctx.model.Experiment.create({"title": title, "showImage": showImage, "url": url, "category": category, "createdAt": new Date()});
    ctx.body = "创建新实验成功";         
  }
}

module.exports = ExperimentController;
```


