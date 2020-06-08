## v-modelディレクティブ

機能的には
```v-model``` = ```v-on``` + ```v-bind```

> ```
> <input v-model="searchText">
> ```
>これは以下と同じことです:
> ```
> <input
>  v-bind:value="searchText"
>  v-on:input="searchText = $event.target.value"
>```
https://jp.vuejs.org/v2/guide/components.html
