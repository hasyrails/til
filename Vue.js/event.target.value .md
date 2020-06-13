## フォーム入力の値を取得する

> ```HTML
> <input v-bind:value="message" v-on:change="handleInput">
> ```

> ```JavaScript
> new Vue({
>   el: '#app',
>   data: {
>     message: 'Hello Vue.js',
>   },
>   methods: {
>     handleInput: function (event) {
>       // 代入前に何か処理を行う…
>       this.message = event.target.value
>     }
>   }
> })
> ```

https://cr-vue.mio3io.com/guide/chapter3.html#%E3%83%95%E3%82%A9%E3%83%BC%E3%83%A0%E5%85%A5%E5%8A%9B%E3%81%AE%E5%8F%96%E5%BE%97

