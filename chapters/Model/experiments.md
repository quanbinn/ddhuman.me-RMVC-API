# experiments

### app/controller/experiments.js

#### schema

```javascript
const experimentSchema = new mongoose.Schema({
  title: String, 
  showImage: String, 
  url: String, 
  createdAt: { type: Date},
  creator: String,
});
```


```javascript
const mongoose = require('mongoose');
mongoose.connect('mongodb://localhost/ddhumanme', {useNewUrlParser: true});

const experimentSchema = new mongoose.Schema({
  title: String, 
  showImage: String, 
  url: String, 
  createdAt: { type: Date},
  creator: String,
});

const Experiment = mongoose.model('Experiment', experimentSchema);

const exp1 = new Experiment({
  title: '用橡皮筋和小塑料棍感受函数某点的切线',
  showImage: 'https://i.ibb.co/3T89n6X/image.png',
  url: 'https://gitee.com/quanbinn/Learn-Mathematical-Olympiad-The-Interactive-Way/blob/master/chapters/%E5%BE%AE%E5%88%86/%E7%94%A8%E6%A9%A1%E7%9A%AE%E7%AD%8B%E5%92%8C%E5%B0%8F%E5%A1%91%E6%96%99%E6%A3%8D%E6%84%9F%E5%8F%97%E5%87%BD%E6%95%B0%E6%9F%90%E7%82%B9%E7%9A%84%E5%88%87%E7%BA%BF.md',
  createdAt: 'Wed Sep 30 2020 17:53:29 GMT+0800 (中国标准时间)', // new Date()
  creator: 'QwkSmREWsw5KDx3L7'  
});

exp1.save().then(() => console.log('done'));
```


