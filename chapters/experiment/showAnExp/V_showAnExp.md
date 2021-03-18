```html
  {% if exp.videoAddr %}
    <video width=100% controls="controls" autoplay="autoplay">
      <source src="{{ exp.videoAddr }}" type="video/mp4">
    </video>
  {% else %}
    <img src="{{ exp.bigImgAddr }}" alt="{{ exp.expname }}" style="width:100%;">
  {% endif %}

  <a href="{{exp.procedureUrl}}">
    <h3>实验步骤：{{ exp.expname }}</h3>
  </a>
```



