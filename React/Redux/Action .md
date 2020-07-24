## Actionの定義
参考：[Action および Action Creator](https://qiita.com/mpyw/items/a816c6380219b1d5a3bf#action-%E3%81%8A%E3%82%88%E3%81%B3-action-creator)

### Actionのフォーマット
> Actionは基本的に以下のようなフォーマットを持つオブジェクトになる。
> ``` js
> {
>    type: "アクションの種類を一意に識別できる文字列またはシンボル",
>    payload: "アクションの実行に必要な任意のデータ",
> }
> ```

### 定義例
``` js
export const addScheduleSetValue = payload => ({
  type: ADD_SCHEDULE_SET_VALUE,
  payload
});
```

```payload```が必要のないアクションの場合は省略できる
