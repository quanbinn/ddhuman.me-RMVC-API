```html
<form  method="POST" action="/admin/experiment/createdForm?_csrf={{ ctx.csrf | safe }}" enctype="multipart/form-data">
    <h3>创建新实验</h3>
    <input type="text" name="expname" placeholder="输入实验名称"><br>
    类型: <select name= "category">
                <option value="实体学习">实体学习</option>
                <option value="拆分工作">拆分工作</option>  
                <option value="极速购物">极速购物</option>
                <option value="防卫锻炼">防卫锻炼</option>
                <option value="健康饮食">健康饮食</option>
                <option value="防病防险">防病防险</option>
        </select><br>

    子类型: <select name= "subcategory">
                <option value="奥数">奥数</option>
                <option value="代数">代数</option>  
                <option value="立体几何">立体几何</option>
                <option value="微分">微分</option>
                <option value="线性代数">线性代数</option>
                <option value="概率">概率</option>
                <option value="统计">统计</option>
                <option value="编程基础">编程基础</option>
                <option value="数据结构">数据结构</option>
                <option value="深度学习">深度学习</option>  
                <option value="强化学习">强化学习</option>
                <option value="机器学习">机器学习</option>                    
                <option value="其他">其他</option>
                <option value="学习道具">学习道具</option>
                <option value="工作用品">工作用品</option>  
                <option value="健身用品">健身用品</option>
                <option value="其他">其他</option>
                <option value="人体解剖">人体解剖</option>
                <option value="其他">其他</option>
                <option value="病理性近视">病理性近视</option>
                <option value="颈椎病">颈椎病</option>  
                <option value="腰椎病">腰椎病</option>
                <option value="其他">其他</option>
        </select><br>

    <input type="text" name="procedureUrl" placeholder="输入外部展示步骤的Url"><br>

    上传小图片: <input type="file" name="smallImgAddr"><br>
    上传大图片: <input type="file" name="bigImgAddr"><br>
    上传视频: <input type="file" name="videoAddr"><br>       

    <button type="submit">创建</button>
</form>
```



