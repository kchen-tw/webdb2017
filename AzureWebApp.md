    # 在 GitHub 中新增 AzureWebApp 專案

* 在 GitHub 建立一個新的 repository ，並且命名為 AzureWebApp
* 利用 GitHub Desktop 同步到本機端
* 建立一個 server.js 內容如下

```js
// 引用 http 模組
var http = require('http')

// 設定 port 預設為 1337，若系統環境有設定則以系統環境設定為主
var port = process.env.PORT || 1337;

// 建立一個 http server
var app = http.createServer(function (req, res) {
    // 回覆 200
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Hello World\n');
})

// 啟動並等待連接
app.listen(port);
console.log('Server running at http://127.0.0.1:' + port);
```

* 將 AzureWebApp 同步到 GitHub

# 在 Azure 上建立 Web應用程式

請參考社團直播影片或下方步驟圖

### **先確認權限：**

Step1.
![](/assets/權限確認.png)

Step2.
![](/assets/權限2.png)

### 進行WEBAPP專案新增：

1.![](/assets/new_1.png)
2.![](/assets/new_2.png)
3.![](/assets/new_3.png)
4.![](/assets/new_4.png)
5.![](/assets/new_5.png)
6.![](/assets/new_6.png)
7.![](/assets/new_7.png)
8.![](/assets/new_8.png)
9.![](/assets/new_9.png)
10.![](/assets/new_10.png)
11.![](/assets/new_19.png)
12.![](/assets/new_11.png)
13.![](/assets/new_13.png)
14.![](/assets/new_14.png)
15.![](/assets/new_15.png)
16.![](/assets/new_16.png)
17.![](/assets/new_17.png)
18.![](/assets/new_18.png)
19.![](/assets/new_20.png)
20.![](/assets/new_21.png)

