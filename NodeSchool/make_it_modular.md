# 第6關: 建立自己的模組

## MakeItModular.js (主程式)
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
## mymodule.js (自訂模組)

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


