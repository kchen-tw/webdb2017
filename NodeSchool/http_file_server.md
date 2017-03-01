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