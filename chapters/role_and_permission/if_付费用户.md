```javascript
    if (ctx.session.role == "付费用户") {
      await ctx.render('...', {key1: value1, title:'...'});
    } else { 
      ctx.redirect("/"); 
    }
```


