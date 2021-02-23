# 理解在session中用cookies存储用户名和密码的原理

![](/images/附录/csrf-cookie-session.jpg)

## 单独使用cookie的原理

1. 浏览器端通过**http的post请求**发送注册或登录时用户名和密码的key-value信息；
2. 服务器端在进行数据库**CRUD**操作的同时，把用户名和密码的key-value信息存在一个**object**（通常需要对密码进行加密）里；
3. 同时把这个**object**回传给浏览器。这个**object**被称为**cookie**。
4. 下一次对域名访问的时候，**这个cookie里面的object信息也会被发送**。

## 在session过程使用cookie的原理
1. 浏览器端通过**http的post请求**发送注册或登录时用户名和密码的key-value信息；
2. 服务器端在进行数据库**CRUD**操作的同时，把用户名和密码的key-value信息存在一个**object**（通常需要对密码进行加密）里，同时随机生成1个加密的**string (SessionID)**, 这些信息放在1个对象里，被称为**session**;
3. 同时把这个**SessionID**的key-value信息回传给浏览器，放在浏览器的cookie中，即：**NameOfSessionID: randomString**;
4. 下一次对域名访问的时候，这个cookie里面**SessionID**的**key-value信息**也会**被浏览器发送给服务器**；
5. 服务器会根据这个**SessionID**的**value值**查找到**对应的用户名和密码的key-value信息**。

```javascript
// clear cookie
async logout(){
	this.ctx.cookies.set('userinfo',null);
	this.ctx.redirect('/news');
}

//option
{
	maxAge:1000*3600*24, // 浏览器存储1天
	httpOnly:true,
	signed:true,
	encrypt:true
}

// get
var userinfo = this.ctx.cookies.get('username',{encrypt:true});
await this.ctx.render('news', {username: userinfo})
// view
{{ username }}

// set(key, value, option)
this.ctx.cookies.set('username', 'yuhangxia', {
	maxAge:1000*3600*24, // 浏览器存储1天
	httpOnly:true,
	signed:true,
	encrypt:true
});

/* cookies is an object. key-value pairs 
可以实现同一个浏览器访问同一个域名的时候，不同页面之间的数据共享。
默认情况cookies在浏览器关闭之后就销毁了
数据加密之后可以设置中文cookie
*/
```

```javascript
// config.default.js
config.session = {
	key: 'SESSION_ID',  // not important
	maxAge: 24*3600*1000,
	httpOnly:true,
	encrypt:true,
	renew:true  	
}

---------------------------------------
this.ctx.session.maxAge = 1000;

this.ctx.session.userinfo = {
	name: yannanwu,
	age; 34
}

let userinfo = this.ctx.session.userinfo;
console.log(userinfo);
---------------------------------------

// set a session
this.ctx.session.username = 'yuhangxia';

//get a session
let username = this.ctx.session.username;
await this.ctx.render('news', {username: username});

{{ username }}
```

## Reference

1. [**Session (computer science)**](https://en.wikipedia.org/wiki/Session_(computer_science))
2. [**Session ID**](https://en.wikipedia.org/wiki/Session_ID)
3. [HTTP cookie](https://en.wikipedia.org/wiki/HTTP_cookie)
4. [**Cross-site request forgery**](https://en.wikipedia.org/wiki/Cross-site_request_forgery)
5. [Egg.js中Cookie的使用](https://www.bilibili.com/video/BV1ub411m7Fs?p=7)
6. [Egg.js中Session的使用](https://www.bilibili.com/video/BV1ub411m7Fs?p=8)

