# experiments

### app/view/users/experiments.tpl

```html
<html>
  <head>
    <title>DDHuman.me</title>
  </head>
  <body>
    <div>
      {% for item in list %}
        <h1>实验名称：{{ item.title }}</h1>
        <a href="{{ item.url }}"><img src="{{ item.showImage }}" alt="{{ item.title }}" width="400"></a>
        <h1><a href="{{ item.url }}">打开链接做实验</a></h1>
        <p>类别：{{ item.tag }}</p>
      {% endfor %}
    </div>
  </body>
</html>
```



