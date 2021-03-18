### this.ctx.model.User == db.users

```javascript
ctx.model.User.updateOne({_id: userId}, 
                                {
                                  $set:{'role': role,"createdAt": new Date()}
                                }
                                );
```

