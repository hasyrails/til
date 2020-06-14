##  spliceメソッド　- つなぎ合わせる -
※ spliceメソッドはJavaScriptに対して定義されているものであり、
  vuex特有のインスタンメソッドというわけではない


### 削除機能のmutations設定
コンポーネントの削除機能を実装する際、

> items 配列 index: 3 の 要素を削除する例  
> ○ spliceを使おう
> ```
> this.items.splice(3, 1);
> ```
https://qiita.com/tmak_tsukamoto/items/e303328681f20a036530

に倣って、
> ```
> mutations: {
>     removelist(state, payload) {
>       state.lists.splice(payload.listIndex, 1)
>     },
>    },
> ```
のように実装
