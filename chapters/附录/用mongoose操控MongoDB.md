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

4. **require("mongoose")** -> **mongoose.connect("dbUrl"))** 

5. **require("mongoose")** -> **mongoose.Schema** -> **let DocumentSchema = new Schema({...})** -> **let  Document = mongoose.model(" Document",  DocumentSchema)**;

6. **let User = require("..//models/user").User;** -> **User.CRUD**

## 打开实验文件

### 调试环境： 
单击右方的[mongoose-example](https://codesandbox.io/s/mongoose-example-1pxqi?file=/src/index.js:237-245)，浏览器里会打开一个新的页面，里面有下面的代码段，如下图所示。

### index.js
```javascript

```

## Reference

1. [**mongoosejs**](https://mongoosejs.com/)
2. [**egg-mongoose**](https://github.com/eggjs/egg-mongoose)



