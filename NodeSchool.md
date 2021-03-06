# 利用 NodeSchool 自我學習

[NodeSchool](https://nodeschool.io/
) 是一個由自願者所推動的開放原始碼專案，主要有兩個目標：『建立高品質的程式開發教材』和『推動教學性的社群活動』

首先選擇要學習項目，這裡我們選擇 `learnyournode`
![](/assets/learn_01.png)

### 安裝 learnyounode
在終於端輸入
```
> npm install -g learnyounode 
```

將 `learnyounode` 套件安裝至全域區
![](/assets/learn_02.png)


### 執行 learnyounode

在終於端輸入
```
> learnyounode 
```

進入到學習選單
![](/assets/learn_03.png)

---

# 開始挑戰

## 第一關：Hello World

```js
console.log("HELLO WORLD");
```

---

## 第二關：Baby Steps

```js
// console.log(process.argv)

var sum = 0;
for(var i=2; i<process.argv.length; i++){
//sum += +process.argv[i];
sum += Number(process.argv[i]);
}
console.log(sum);
```

---

## 第三關：My First I/O

```js
// 引用預設 fs 模組
const fs = require('fs');

// 同步讀取檔案，需等到檔案全部讀取完成才會執行下一行
var buf = fs.readFileSync(process.argv[2]);
// // 若使用 utf8 讀檔
// var buf = fs.readFileSync(process.argv[2], 'utf8');

// 將 Buffer 資料轉成 String
var str = buf.toString();

// 用'\n'切割字串
var lines = str.split('\n');

console.log(lines.length - 1);
```

---


## 第四關: My First Async I/O

```js
// 引用預設 fs 模組
const fs = require('fs');
// 記錄檔案路徑
var path = process.argv[2];
// 讀取檔案，使用非同步函式
fs.readFile(path, (err, data) => {
    if (err) throw err;
    var str = data.toString();
    // 用'\n'切割字串
    var lines = str.split('\n');
    console.log(lines.length - 1);
});

```
---

## 第五關: 非同步過濾副檔名

```js
// 引用預設 fs 模組
const fs = require('fs');
// 引用 path 模組，用來取得副檔名
const path = require('path');
// 記錄檔案路徑
var dir = process.argv[2];
// 記錄副檔案
var ext = '.' + process.argv[3];

// 讀取檔案，使用非同步函式
fs.readdir(dir, (err, files) => {
    if (err) console.error(err);
    var length = files && files.length;
    if (!length) {
        return;
    }

    var result = [];

    // for(var i=0; i<length; i++) {
    //      var filePath = files[i];
    //      if(path.extname(filePath) === ext) {
    //          result.push(filePath);
    //      }
    // }

    // 另一種寫法
    files.forEach((file, index) => {
        if (path.extname(file) === ext) {
            result.push(file);
        }
    });

    console.log(result.join('\n'));
});
```

---

## 第六關: 建立自己的模組

### MakeItModular.js (主程式)
```js
var dir = process.argv[2],
    ext = process.argv[3],
    mymodule = require('./mymodule.js');

mymodule(dir, ext, function (err, data) {
    if (err) {
        console.log(err);
        return;
    }
    console.log(data.join('\n'));
});
```
### mymodule.js (自訂模組)

```js
module.exports = function(dir, ext, callback) {
    var fs = require('fs'),
        path = require('path'),
        result = [];
    fs.readdir(dir, function(err, files) {
        if (err) return callback(err);
        var length = files && files.length;
        for(var i = 0; i < length; ++i) {
            var filePath = files[i];
            if(path.extname(filePath).substr(1) === ext) {
                result.push(filePath);
            }
        }
        callback(null, result);
    })
};
```

---


## 第11關: HTTP FILE SERVER


```js
var http = require('http'),
    fs = require('fs'),
    port = process.argv[2],
    path = process.argv[3],
    server = http.createServer(function(req, res) {
        var fsStream = fs.createReadStream(path);
        fsStream.pipe(res);
    });
server.listen(port);
```

---

## 第12關: HTTP UPPERCASERER


```js
var http = require('http'),
    port = process.argv[2],
    map = require('through2-map'),
    server = http.createServer(function (req, res) {
        if (req.method != 'POST')
            return res.end('send me a POST\n')
        req.pipe(map(function (chunk) {
            return chunk.toString().toUpperCase();
        })).pipe(res);
    });
server.listen(port);
```

---

## 第13關: HTTP JSON API SERVER

```js
var http = require('http'),
    url = require('url'),
    port = process.argv[2],
    server = http.createServer(function (req, res) {
        res.writeHead(200, { 'Content-Type': 'application/json' });
        if (req.method != 'GET') {
            return res.end('send me a GET\n');
        }
        var _urlObj = url.parse(req.url, true),
            _path = _urlObj.pathname,
            _originTime = _urlObj.query.iso,
            _date,
            _result;
        if (!_originTime) {
            return res.end('no query string \'iso\'\n');
        }
        _date = new Date(_originTime);
        if (_path === '/api/parsetime') {
            _result = JSON.stringify({
                hour: _date.getHours(),
                minute: _date.getMinutes(),
                second: _date.getSeconds()
            });
        } else if (_path === '/api/unixtime') {
            _result = JSON.stringify({
                unixtime: _date.getTime()
            });
        } else {
            _result = 'illegal request path!\n';
        }
        return res.end(_result);
    });
server.listen(port);
```











