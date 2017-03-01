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




