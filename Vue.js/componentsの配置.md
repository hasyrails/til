## ```<template>```と```<script>```を使ってcomponentを配置する

component配置のテンプレート
```JavaScript
<template>
// HTMLを書く //
</template>

<script>
// JSを書く //
</script>
```

## ```export default```で```import```呼出可のcomponentに設定する

```<script>```タグ内で
```export defaurt```と宣言すると
他のcomponentから呼び出されることが可能になる。

```JavaScript
// ImportedComponent.vue

<template>
  <div id="app">
    <p>Please import</p>
  <id>
</templare>

<script>
export default {
}
</script>
```

## ```import from```で他のcomponentをimportする

```JavaScript
<template>
  <div id="app">
  　<!-- ImportedComponentコンポーネント呼び出し -->
    <board />
  </div>
</template>

<script>
// インポート文を追加
import ImportedComponent from './components/ImportedComponent.vue'

export default {
  name: 'app',
  components: {
    // Importedコンポーネントに登録する
    ImportedComponent
  }
}
</script>
```
