```javascript
module.exports = app => {
  const mongoose = app.mongoose;
  const Schema = mongoose.Schema;
    
  const ExperimentSchema = new Schema({
      expname: { type: String }, 
      smallImgAddr: { type: String }, 
      bigImgAddr: { type: String },       
      videoAddr: { type: String },            
      procedureUrl: { type: String },
      category: { type: String }, 
      subcategory: { type: String },         
      createdAt: { type: Date},
  });

  return mongoose.model('Experiment', ExperimentSchema);
}
```

