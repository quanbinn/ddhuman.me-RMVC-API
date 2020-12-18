# 体验提交form发送post请求的原理

## 提交form发送post请求的核心逻辑

1. action="http://114.116.231.109/action_page.php"
2. method="post"

```html
<!DOCTYPE html>
<html>
<body>

<form action="http://114.116.231.109/action_page.php" method="post">
First name:<input type="text" id="fname" name="fname"><br><br>
Last name:<input type="text" id="lname" name="lname"><br><br>
<input type="submit" value="Submit">
</form>

</body>
</html>
```

## Reference

1. [**Forms from w3.org**](https://www.w3.org/TR/html401/interact/forms.html)
2. [form method Attribute](https://www.w3schools.com/tags/tryit.asp?filename=tryhtml_form_method)
3. [Egg.js Post提交数据，安全机制CSRF的防范，以及配置模板全局变量](https://www.bilibili.com/video/BV1ub411m7Fs?p=6)

