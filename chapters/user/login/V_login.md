```html
<form action="/user/loginedForm" method="POST">
  <h3>登录</h3>
  <input type="hidden" name="_csrf" value="{{csrf}}">
  <input type="text" name="username" placeholder="输入用户名" required><br>
  <input type="password" name="password" placeholder="输入密码" required><br>
  <button type="submit">登录</button>
</form>
```

