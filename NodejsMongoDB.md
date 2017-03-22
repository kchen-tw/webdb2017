# Node.js 與 MongoDB

## MongoDB 安裝

```
npm install mongodb
```

## 宣告 MongoClient 變數

```js
var MongoClient = require('mongodb').MongoClient;
```

## 宣告 Azure 主機字串

```js
var url = 'mongodb://<endpoint>:<password>@<endpoint>.documents.azure.com:10250/?ssl=true';
```

## 連接 MongoDB 主機

```js
MongoClient.connect(url, function(err, db) {
  console.log('主機連線成功');
  db.close();
});
```

## 參考資料

* 官網文件：https://docs.mongodb.com/getting-started/node/client/
* GitHub範例：https://github.com/kchen-tw/webdb2017-mongodb/