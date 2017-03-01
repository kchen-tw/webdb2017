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