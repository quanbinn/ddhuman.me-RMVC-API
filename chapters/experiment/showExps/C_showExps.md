```javascript
const Controller = require('egg').Controller;

class ExperimentController extends Controller {

  async showMathematicalOlympiad() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "奥数"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示奥数'});
  };

  async showAlgebra() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "代数"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示代数'});
  };

  async showDifferentialCalculus() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "微分"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示微分'});
  };    

  async showLinearAlgebra() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "线性代数"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示线性代数'});
  };     

  async showProbability() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "概率"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示概率'});
  };       

  async showStatistics() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "统计"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示统计'});
  };       

  async showDeepLearning() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "深度学习"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示深度学习'});
  };       

  async showReinforcementLearning() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "强化学习"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示强化学习'});
  };       

  async showProgrammingBasics() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "编程基础"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示编程基础'});
  };    

  async showDataStructure() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "数据结构"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示数据结构'});
  };    

  async showPathologicalMyopia() { const { ctx } = this;
    const experiments = await ctx.model.Experiment.find({subcategory: "病理性近视"});
    await ctx.render('experiment/showSubcategory.tpl', {list: experiments,title:'显示病理性近视'});
  };  

}

module.exports = ExperimentController;
```


