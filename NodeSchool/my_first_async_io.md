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




