```html
      <form  method="POST" action="/order/createdForm">
        <input type="hidden" name="_csrf" value="{{csrf}}"> 

        <h3>成为付费会员</h3>
        
        会员总时间： <span name="plan_time">1</span>个月<br>
        金额： <span name="plan_price">9</span>元<br>
        类型: <span name="pay_category">付费会员</span><br>

        <button type="submit">支付宝付款</button>
      </form>
```



