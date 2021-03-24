```javascript
module.exports = app => {
  const mongoose = app.mongoose;
  const Schema = mongoose.Schema;
    
  const OrderSchema = new Schema({
      username: { type: String, required:true, unique:true },
      amount: { type: Number, required:true },   
      category: { type: String },   
      createdAt: { type: Date, required:true},
      expirationAt: { type: Date, required:true},
  });

  return mongoose.model('Order', OrderSchema);
}
```

