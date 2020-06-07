## v-onディレクティブ　- イベント発火時のメソッド呼出 -

### 例
clickイベントが発火した時SomeMethodメソッドが実行されるようにする
```
<div id="app">
  <button v-on:click="SomeMethod">Click</button>
<div>
```

```
var example_v-on = new Vue({
  el: '#app',
  methods: {
    SomeMethod: function(){
    # clickイベントが起きた時の処理
    }
  }
})
```

### 対応させれるイベントはいろいろあり
```
v-on:(event)
```

https://blog.capilano-fw.com/?p=2787
