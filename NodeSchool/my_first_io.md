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

console.log(lines.length-1);
```




