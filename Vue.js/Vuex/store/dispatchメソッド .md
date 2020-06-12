##  dispathメソッド -アクションを呼び出す-

### Vuexのどこの話？
> Vuexでのデータの流れは Actions → Mutations → State → Vue Components となります。
> それぞれの名前が違うだけでFluxの考え方を素直に取り入れている感じがします。

https://qiita.com/nasum/items/d17c0a628e6c32616b85

### 例

> dispatchはアクションを呼び出すメソッドです。
> コンポーネントのmethodsで、下記の様に使用します。

> ```Vue
> methods: {
>     clickPlus() {
>       this.$store.dispatch('increment')
>     },
>     clickMinus() {
>       this.$store.dispatch('decrement')
>     }
> ```

https://junpeko.com/vuex-actions/
