## mapStateヘルパー -computedプロパティないで使用できる省略記法-

> ```
> //mapStateヘルパー利用
> computed: mapState(['count'])
> 
> //mapStateヘルパーを利用しない場合
> computed : {
>   count : function(){
>     return this.$store.state.count
>   }
> }
> ```
https://reffect.co.jp/vue/vue-js-vuex-map-helper
