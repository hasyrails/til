## MDN
https://developer.mozilla.org/ja/docs/Web/API/Storage/setItem

> Storage インターフェイスの setItem() メソッドは
> キーの名称と値を渡すと、
> ストレージにキーを追加する、またはキーがすでに存在する場合はキーに対する値を更新します。

> ```
> storage.setItem(keyName, keyValue);
> ```

>例

> ```
> function populateStorage() {
>   localStorage.setItem('bgcolor', 'red');
>   localStorage.setItem('font', 'Helvetica');
>   localStorage.setItem('image', 'myCat.png');
> }
> ```

## Strageインターフェース
localStorageだけでなく
sessionStorageとかも入る。

https://www.w3schools.com/jsref/met_storage_setitem.asp
