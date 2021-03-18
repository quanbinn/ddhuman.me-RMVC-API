### this.ctx.model.User == db.users

```javascript
ctx.model.User.create({
                               "username": username, 
                                "password": password,
                                "role": "普通用户", 
                                "createdAt": new Date()
                            });
```

