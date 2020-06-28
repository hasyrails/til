## Redux lifecycle

```
{ [Action] ▶︎　[Reducer] ▶︎　[Store] ▶︎　[View] } ▶︎　{ [Action] ▶︎ ‥‥
```

### すごいQiitaがあるもんだ
Redux入門ダイジェスト版
https://qiita.com/kitagawamac/items/49a1f03445b19cf407b7

### Actions
>actionはアプリケーションからの情報をstoreへ送る為のオブジェクト  
>actionは store.dispatch()でstoreへ送られます　　
https://qiita.com/kitagawamac/items/8f8d047e5cbd87399ccb

### Reducers
> reducerは、actionを受けてstateを変更するの為のメソッドです　　
https://qiita.com/kitagawamac/items/7fdce94912d6d9c801f8

### Stores
> Storesの役割は、
> ・stateを保持する
> ・stateへアクセスするためのgetState()を提供する
> ・stateを更新するためのdispatch(action)を提供する
> ・リスナーを登録するためのsubscribe(listener)を提供する　　
https://qiita.com/kitagawamac/items/377787c24efac64f2495　
