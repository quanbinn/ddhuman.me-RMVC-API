```html
<html>
  <head>
    <title>创建新实验</title>
  </head>

  <body>
      <h2>创建新实验</h2>
      <form action="/experiment/createdForm" method="POST">
        <input type="hidden" name="_csrf" value="{{csrf}}">
        实验名称: <input type="text" name="title"><br>
        展示图片地址: <input type="text" name="showImage"><br>
        外部展示步骤Url: <input type="text" name="url"><br>
        类型: <input type="text" name="category"><br>
        <button type="submit">创建</button>
      </form>
  </body>
</html>
```



