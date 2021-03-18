```html
      <form  method="POST" action="/admin/experiment/editedForm/{{exp._id}}?_csrf={{ ctx.csrf | safe }}" enctype="multipart/form-data">

        实验名称： <input type="text" name="expname" value="{{exp.expname}}"><br>
 		类型: <select name= "category" >
	              <option value="{{exp.category}}" selected>{{exp.category}}</option>			
	              <option value="实体学习">实体学习</option>
	              <option value="拆分工作">拆分工作</option>  
	              <option value="极速购物">极速购物</option>
	              <option value="防卫锻炼">防卫锻炼</option>
	              <option value="健康饮食">健康饮食</option>
	              <option value="防病防险">防病防险</option>        
			  </select><br>

		子类型: <select name= "subcategory" >
			 	  <option value="{{exp.subcategory}}" selected>{{exp.subcategory}}</option>
	              <option value="奥数">奥数</option>
	              <option value="代数">代数</option>  
	              <option value="立体几何">立体几何</option>
	              <option value="微分">微分</option>
	              <option value="线性代数">线性代数</option>
	              <option value="概率">概率</option>
	              <option value="统计">统计</option>
	              <option value="深度学习">深度学习</option>  
	              <option value="强化学习">强化学习</option>
	              <option value="机器学习">机器学习</option>
	              <option value="数据结构">数据结构</option>
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

        外部展示步骤的Url： <input type="text" name="procedureUrl" value="{{exp.procedureUrl}}"><br>

        再次上传小图片: <input type="file" name="smallImgAddr"><br>
        再次上传大图片: <input type="file" name="bigImgAddr"><br>
        再次上传视频: <input type="file" name="videoAddr"><br>       

        <button type="submit">更新</button>
      </form>
```



