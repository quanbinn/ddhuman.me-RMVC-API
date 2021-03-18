```javascript
module.exports = app => {
  const mongoose = app.mongoose;
  const Schema = mongoose.Schema;
    
  const GoodsSchema = new Schema({
      goodsname: { type: String }, 
      smallImgAddr: { type: String }, 
      bigImgAddr: { type: String },       
      purchaseUrl: { type: String },
      category: { type: String }, 
      subcategory: { type: String },         
      createdAt: { type: Date},
  });

  return mongoose.model('Goods', GoodsSchema);
}
```

