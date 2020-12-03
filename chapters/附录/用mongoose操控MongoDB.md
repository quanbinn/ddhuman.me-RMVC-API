# 用mongoose操控MongoDB

## 安装MongoDB后用mongoose库操作它的核心逻辑

1. 在web上下载相应的MongoDB版本到Ubuntu版本的服务器 (文件集合)，然后安装到Ubuntu里；

   ```
   $ sudo apt-get install mongodb
   ```

2. 在服务器上运行MongoDB（文件集合），生成了用javascript函数调用的API；

   ```
   $ sudo service mongodb status
   $ sudo service mongodb start
   ```

3. 安装mongoose库，生成了用nodejs函数调用MongoDB的API；

   ```
   $ npm i egg-mongoose --save
   ```

4. require("mongoose")	->	mongoose.connect("**dbUrl**"))

5. const **documentSchema** = new **mongoose.Schema**({...})

	->	const **Collection** = mongoose.model("**Collection**",  **documentSchema**);

6. **Collection**.**CRUD**

## 打开实验文件

### 调试环境： 
单击右方的[mongoose-example](https://codesandbox.io/s/mongoose-example-1pxqi?file=/src/index.js:237-245)，浏览器里会打开一个新的页面，里面有下面的代码段，如下图所示。

### mongoose-first-example.js
```javascript
const mongoose = require('mongoose');
mongoose.connect('mongodb://localhost:27017/test', {useNewUrlParser: true, useUnifiedTopology: true});

const Cat = mongoose.model('Cat', { name: String });

const kitty = new Cat({ name: 'Zildjian' });
kitty.save().then(() => console.log('meow'));
```

### tutorial.js
```javascript
const mongoose = require('mongoose');
mongoose.connect('mongodb://localhost/test', {useNewUrlParser: true});

const db = mongoose.connection;
db.on('error', console.error.bind(console, 'connection error:'));
db.once('open', function() {
	const kittySchema = new mongoose.Schema({
	  name: String
	});

	kittySchema.methods.speak = function () {
	  const greeting = this.name
	    ? "Meow name is " + this.name
	    : "I don't have a name";
	  console.log(greeting);
	}

	const Kitten = mongoose.model('Kitten', kittySchema);

	const silence = new Kitten({ name: 'Silence' });
	console.log(silence.name); // 'Silence'

	const fluffy = new Kitten({ name: 'fluffy' });
	fluffy.speak(); // "Meow name is fluffy"

	fluffy.save(function (err, fluffy) {
	if (err) return console.error(err);
	fluffy.speak();
	});

	Kitten.find(function (err, kittens) {
	  if (err) return console.error(err);
	  console.log(kittens);
	})

});
```

## Reference

1. [**mongoosejs**](https://mongoosejs.com/)
2. [**egg-mongoose**](https://github.com/eggjs/egg-mongoose)



