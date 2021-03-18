```html
      <form  method="POST" action="/admin/goods/createdForm?_csrf={{ ctx.csrf | safe }}" enctype="multipart/form-data">
        <h3>创建新商品</h3>
        <input type="text" name="goodsname" placeholder="输入商品名称"><br>
        类型: <select name= "category">
                    <option value="极速购物">极速购物</option>
            </select><br>

        子类型: <select name= "subcategory">
                    <option value="学习道具">学习道具</option>
                    <option value="工作用品">工作用品</option>  
                    <option value="健身用品">健身用品</option>
                    <option value="其他">其他</option>    
            </select><br>

        <input type="text" name="purchaseUrl" placeholder="输入购买商品的Url"><br>

        上传小图片: <input type="file" name="smallImgAddr"><br>
        上传大图片: <input type="file" name="bigImgAddr"><br> 

        <button type="submit">创建</button>
      </form>
```



