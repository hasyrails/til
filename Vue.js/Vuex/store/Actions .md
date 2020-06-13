## Actions - Mutationsを実行(Commit) -

```Vue.js 
// ===Vuex storeの雛形コード===

import Vue from 'vue'
import Vuex from 'vuex'

Vue.use(Vuex)

export default new Vuex.Store({
  state: {
  },
  mutations: {
  },
  actions: {
  },
  modules: {
  }
})
```

```Actions -(Mutationsを実行)→ Mutations```というMutationsに指令を出す関係

## Actionsの設定例

Actionsの設定に合わせたMutationsの設定も合わせて

```Vue.js

export default new Vuex.Store({
  state: {
  },
  mutations: {
    addlist(state, payload) {　　　　　　//第１引数state ： stateで定義する変数
    　　　　　　　　　　　　　　　　　　　　　//第２引数payload : actionsからのcommitで受け取った引数  
      state.lists.push({ title: payload.title, cards:[] })
  },
  actions: {
    addlist(context, payload) {        //第１引数context : ストアインスタンスのメソッド、プロパティを呼び出せるオブジェクト
    　　　　　　　　　　　　　　　　　　　　　//第2引数payload : mutationに渡す引数
      
      context.commit('addlist', payload)
  },
  modules: {
  }
})

```
