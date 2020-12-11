```html
<html>
  <head>
    <title>DDHuman.me</title>
  </head>
  <body>
  	<ul>
      {% for item in list %}
      	<li>
      		<a href="{{ item.url }}">{{ item.title }}</a>
			<a href="{{ item.url }}"><img src="{{ item.showImage }}" alt="{{ item.title }}" width="200"></a>
      	</li>
      {% endfor %}  		
  	</ul>
  </body>
</html>
```



