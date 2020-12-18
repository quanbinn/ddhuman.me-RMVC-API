# 实现responsive_layout中各网页元素的width占比

## 核心逻辑

1. width: 30% (percent)

单击右方的[在线代码段Url网址](https://codepen.io/quanbinn/pen/QBBmmL)，浏览器里会打开一个新的页面，里面有下面的代码段。

```css
.column{
  float: left; text-align: center; 
  height: 150px; 
}

.left, .right{width: 30%}
.middle{width: 40%}

span {
    float: right;
}
```

```html
<html>
  <head>
    <title>首页</title>
    <link rel="stylesheet" type="text/css" href="public/css/style.css">
  </head>

  <body>
	<div>
	    <div class="column left">
	      <h1><a href="/experiments">交互式学习</a></h1>
	    </div>
	    <div class="column middle"></div>  
	    <div class="column right">
	      <h1><a href="">极简工作</a></h1>
	    </div>
	  </div>

	  <div>
	    <div class="column left"></div>
	    <div class="column middle">
	      <h1><a href="">极速购物</a></h1></div>  
	    <div class="column right"></div>
	  </div>

	  <div>
	    <div class="column left">
	      <h1><a href="">健康饮食</a></h1> 
	    </div>
	    <div class="column middle"></div>  
	    <div class="column right">
	      <h1><a href="">防病防险</a></h1>
	      <h1><a href="">防卫性锻炼</a></h1>
	    </div>
	  </div>
  </body>
</html>
```

## Reference

1. [.class, #id from CSS](https://en.wikipedia.org/wiki/CSS)
2. [**Responsive web design from Wikipedia**](https://en.wikipedia.org/wiki/Responsive_web_design)
3. [*.class* Selector](https://www.w3schools.com/cssref/sel_class.asp)
4. [#*id* Selector](https://www.w3schools.com/cssref/sel_id.asp)
5. [**What is Responsive Web Design?**](https://www.w3schools.com/whatis/whatis_responsive.asp)
6. [**W3.CSS Framework**](https://www.w3schools.com/w3css/default.asp)

