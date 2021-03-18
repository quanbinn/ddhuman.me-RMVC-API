```html
<form action="/user/registerdForm" method="POST" onsubmit="return validate()">
  <h3>注册</h3>
  <input type="hidden" name="_csrf" value="{{csrf}}">
  <input type="text" name="username" placeholder="输入用户名" minlength="6" maxlength="16" required><br>
  <input type="password" name="password" placeholder="输入密码" minlength="8" maxlength="16" required><br>
  <button type="submit">提交</button>
</form>
```



