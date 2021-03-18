```html
	<div style="display:flex; flex-wrap:wrap; align-items:center;">	
	      {% for item in list %}
			<div class="textOverImage">
	          <a href="/experiment/{{ item._id }}">
	          	<img src="{{ item.smallImgAddr }}" alt="{{ item.expname }}" style="width:100%; " >
	          </a>

	          <a href='{{_subcategoryUrl[item.subcategory]}}'>
	          	<span class="top-right">{{ item.subcategory }}</span>
	          </a>

	          <a href="/experiment/{{ item._id }}">
		        <span class="centered-medium">{{ item.expname }}</span>
	          </a>

			</div>
	      {% endfor %}      
    </div>
```

```html
	<div style="display:flex; flex-wrap:wrap; align-items:center;">	
	      {% for item in list %}
			<div class="textOverImage">
	        	<a href="/experiment/{{ item._id }}">  
	          		<img src="{{ item.smallImgAddr }}" alt="{{ item.expname }}" style="width:100%; " >
	          	</a>

	        	<a href="/experiment/{{ item._id }}">  
	          		<span class="centered-medium">{{ item.expname }}</span>
	          	</a>        	
			</div>
	      {% endfor %}      
    </div>
```


