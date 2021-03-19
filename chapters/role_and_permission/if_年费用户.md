```javascript
    if (ctx.session.role == "年费用户") {
      await ctx.render('...', {key1: value1, title:'...'});
    } else { 
      ctx.redirect("/"); 
    }
```


