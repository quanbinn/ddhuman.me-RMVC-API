```javascript
    if (ctx.session.role == "超级管理员") {
      await ctx.render('user/adminShowAll.tpl', {"list": users, title:'显示所有用户'});
    } else { 
      ctx.redirect("/"); 
    }
```


