## subscribeメソッド - ストアへのmutationsを読み込む -

ストアのインスタンスメソッド
全てのmutationsが終わった後、
全てのmutationsを読み込む

> ```Vue.js
> store.subscribe((mutation, state) => {
>   console.log(mutation.type)　　　 
>   console.log(mutation.payload)　
> })
> ```

https://vuex.vuejs.org/ja/api/#subscribe
