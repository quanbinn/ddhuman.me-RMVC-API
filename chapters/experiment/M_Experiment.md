```javascript
module.exports = app => {
  const mongoose = app.mongoose;
  const Schema = mongoose.Schema;
    
  const ExperimentSchema = new Schema({
      title: { type: String }, 
      showImage: { type: String }, 
      url: { type: String }, 
      createdAt: { type: Date},
      creator: { type: String },
  });

  return mongoose.model('Experiment', ExperimentSchema);
}
```

