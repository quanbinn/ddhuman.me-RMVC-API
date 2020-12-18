# 理解在session中用cookies存储用户名和密码的原理

1. 浏览器端通过**http的post请求**发送注册或登录时用户名和密码的key-value信息；
2. 服务器端在进行数据库**CRUD**操作的同时，把用户名和密码的key-value信息存在一个**object**（通常需要对密码进行加密）里；
3. 同时把这个**object**回传给浏览器。这个**object**被称为**cookie**。
4. 下一次对域名访问的时候，**这个cookie里面的object信息也会被发送**。



单击右方的[在线代码段Url网址]()，浏览器里会打开一个新的页面，里面有下面的代码段。

```css

```

```html

```

## Reference

1. [****](https://en.wikipedia.org/wiki/Role-based_access_control)

