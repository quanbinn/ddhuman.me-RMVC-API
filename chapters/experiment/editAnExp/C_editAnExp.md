```javascript
const path=require('path');
const fs=require('fs');
const pump = require('mz-modules/pump');

const Controller = require('egg').Controller;

class ExperimentController extends Controller {

  async editExpData() { const { ctx } = this;      
    let expId = ctx.params.id;

    const parts = ctx.multipart({ autoFields: true });

    let stream;
    while ((stream = await parts()) != null) {
        if (!stream.filename) { 
          return;
        }       

        const target = 'app/public/upload/'+parts.field['category']+'/'+parts.field['subcategory']+'/'+parts.field['expname']+'/'+path.basename(stream.filename);
        parts.field[stream.fieldname] = target.replace("app","");         

        const writeStream = fs.createWriteStream(target);
        await pump(stream, writeStream);  
    };

    delete parts.field["_csrf"];       //let {} = parts.field;

    await ctx.model.Experiment.findOneAndUpdate({_id: expId}, {
                                        ...parts.field,     // grammar sugar                                  
                                       "createdAt": new Date(),
                                     });
    ctx.redirect("/admin/experiment/adminShowAll");          
  };


}

module.exports = ExperimentController;
```


