```javascript
const Controller = require('egg').Controller;

class ExperimentController extends Controller {

  async removeExpData() { const { ctx } = this;      
    let expId = ctx.params.id;
    await ctx.model.Experiment.deleteOne({_id: expId});
    ctx.redirect("/admin/experiment/adminShowAll");      
  };  

}

module.exports = ExperimentController;
```


