## arrow関数

https://qiita.com/niisan-tokyo/items/4aec6e01c2c8ffc5fc73#%E7%9C%81%E7%95%A5%E5%BD%A2

## arrow関数の基本形

```javascript
// == 通常表記 ==
function(param1, param2, ...){
  //処理内容
}

// == arrow関数による省略表記 == 
(param1, param2, ...) => {
  //処理内容
}
```
## 省略できるパターン - 引数が１つのとき - 
```js
// == arrow関数表記（引数が１つのとき） == 
(param) => {
  //処理内容
}

// == 省略形 == 
param => {
  //処理内容
}

// == 引数が１つもない時は()省略不可== 
（） => {
  //処理内容
}

```

例
```js
const square = n =>{
  console.log(n * n);
}

const yeah = () =>{
  console.log("yeah!");
}
```
