# 在 Azure 上建立 Web應用程式

## 新增 AzureWebApp 專案

### 雲端 GitHub 
* 在 GitHub 建立一個新的 repository ，並且命名為 AzureWebApp
* 利用 GitHub Desktop 同步到本機端

### 本機端 Visual Studio Code
* 用 Visual Studio Code ，以資料夾的方式開啟
* 建立一個 server.js 內容如下

```js
// 引用 http 模組
var http = require('http')

// 設定 port 預設為 1337，若系統環境有設定則以系統環境設定為主
var port = process.env.PORT || 1337;

// 建立一個 http server
var app = http.createServer(function (req, res) {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Hello World\n');
})

// 啟動並等待連接
app.listen(port);
console.log('Server running on port ' + port);
```

另一種寫法
