```html
<html>
  <head>
    <title>登录</title>
  </head>

  <body>
  <form action="/loginedForm" method="POST">
    <input type="hidden" name="_csrf" value="{{csrf}}">
    用户名: <input type="text" name="username"><br>
    密码: <input type="password" name="password"><br>
    <button type="submit">登录</button>
  </form>
  </body>
</html>
```

