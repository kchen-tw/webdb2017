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
if(!length) {
return;
}

var result = [];

// for(var i=0; i<length; i++) {
// var filePath = files[i];
// if(path.extname(filePath) === ext) {
// result.push(filePath);
// }
// }

// 另一種寫法
files.forEach((file, index) => {
if(path.extname(file) === ext) {
result.push(file);
}
});

console.log(result.join('\n'));
});
```






