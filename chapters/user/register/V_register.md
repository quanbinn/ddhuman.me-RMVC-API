```html
<html>
  <head>
    <title>注册</title>
  </head>

  <body>
  <form action="/registeredForm" method="POST">
    <input type="hidden" name="_csrf" value="{{csrf}}">
    用户名: <input type="text" name="username"><br>
    密码: <input type="password" name="password"><br>
    <button type="submit">注册</button>
  </form>
  </body>
</html>
```



