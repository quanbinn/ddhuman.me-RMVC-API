# 体验移植MongoDB中documents的原理

## 移植MongoDB中所有collections中的所有documents的核心逻辑

1. 把MongoDB的Database中的**所有collections**中的**所有documents（JSON数据结构）取出放在一个数组中**；

   ```javascript
   collection1 = [{},{},{},...,{}], 
   collection2 = [{},{},{},...,{}], 
   collection3 = [{},{},{},...,{}], 
   ... , 
   collectionN =[{},{},{},...,{}]
   ```

2. 把数组放到一个**操作系统中的文件**（例如data.csv后缀名）中；

   ```javascript
   data.csv = ( collection1 = [{},{},{},...,{}], collection2 = [{},{},{},...,{}], collection3 = [{},{},{},...,{}], ... , collectionN =[{},{},{},...,{}] )
   ```

3. 在另外一个**操作系统中读取这个文件**（例如data.csv）；

   ```javascript
   collection1 = [{},{},{},...,{}], 
   collection2 = [{},{},{},...,{}], 
   collection3 = [{},{},{},...,{}], 
   ... , 
   collectionN =[{},{},{},...,{}]
   ```

4. 把所有的数据写入新的MongoDB中。

   ```javascript
   use database；
   db.collection1.insertMany({},{},{},...,{});
   db.collection2.insertMany({},{},{},...,{});
   db.collection3.insertMany({},{},{},...,{});
   ... , 
   db.collectionN.insertMany({},{},{},...,{});
   ```
