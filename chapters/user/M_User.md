```javascript
module.exports = app => {
  const mongoose = app.mongoose;
  const Schema = mongoose.Schema;

  const UserSchema = new Schema({
    username: { type: String, required:true, unique:true,},
    password: { type: String, required:true },
    role: { type: String },
    createdAt: { type: Date},
  });

  return mongoose.model('User', UserSchema);
}
```

