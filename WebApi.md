# WebApi 專案

## MongoDB Server 的設定

### Server 的程式

```
"C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --dbpath .\database
```

### Client 的程式

```
"C:\Program Files\MongoDB\Server\3.4\bin\mongo.exe" --host 127.0.0.1
```

### Client 的指令

查看有那些 database
```
show dbs
```

使用或建立 school 資料庫
```
use school
```

準備要新增的 document
```js
{"sid":"s001","name":"張三"}
```

新增準備好的 document
```
db.student.insert({"sid":"s001","name":"張三"})
```

查詢是否新增成功
```
db.student.find()
```

離開Client程式
```
exit
```

## Node.js 的設定

建立專案 package.json
```
npm init
```

安裝 mongoDB driver
```
npm install mongodb --save
```

宣告 MongoClient 變數

```js
var MongoClient = require('mongodb').MongoClient;
```

宣告 Azure 主機字串

```js
var url = 'mongodb://<endpoint>:<password>@<endpoint>.documents.azure.com:10250/?ssl=true';
```

宣告本機字串
```js
var url = 'mongodb://127.0.0.1/school';
```

連接 MongoDB 主機
```js
MongoClient.connect(url, function(err, db) {
console.log('主機連線成功');
db.close();
});
```
## 定義 WebApi

### 查詢學生資料
```
http://127.0.0.1:1337/find/student
```

### 新增學生資料使用 post
```
http://127.0.0.1:1337/insert/student/
```

key | value
:--:|:-----:
s001| 李四

表單範例
```html
<form action="http://127.0.0.1:1337/insert/student/" method="post">
    學號：<input type="text" name="sid"><br>
    姓名：<input type="text" name="name">
    <input type="submit" value="Submit">
</form>
```

### 新增學生資料使用 get

```
http://127.0.0.1:1337/insert/student/?sid=s001&name=李四
```

### 新增學生資料直接使用 url

```
http://127.0.0.1:1337/insert/student/s001/李四
```


## GitHub 參考資料

* WebApi範例 (https://github.com/kchen-tw/webdb2017-webapi)
* HttpServer範例 (https://github.com/kchen-tw/webdb2017-httpserver)
* MongoDB範例 (https://github.com/kchen-tw/webdb2017-mongodb)