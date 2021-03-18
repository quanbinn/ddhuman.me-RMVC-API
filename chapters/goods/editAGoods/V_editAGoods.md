```html
      <form  method="POST" action="/admin/goods/editedForm/{{goods._id}}?_csrf={{ ctx.csrf | safe }}" enctype="multipart/form-data">

        商品名称： <input type="text" name="goodsname" value="{{goods.goodsname}}"><br>
        类型: <select name= "category" >
                <option value="{{goods.category}}" selected>{{goods.category}}</option>     
                <option value="极速购物">极速购物</option>
        </select><br>

    子类型: <select name= "subcategory" >
                <option value="{{goods.subcategory}}" selected>{{goods.subcategory}}</option>
                <option value="学习道具">学习道具</option>
                <option value="工作用品">工作用品</option>  
                <option value="健身用品">健身用品</option>
                <option value="其他">其他</option>    
        </select><br>

        购买商品的Url： <input type="text" name="purchaseUrl" value="{{goods.purchaseUrl}}"><br>

        再次上传小图片: <input type="file" name="smallImgAddr"><br>
        再次上传大图片: <input type="file" name="bigImgAddr"><br> 

        <button type="submit">更新</button>
      </form>
```



