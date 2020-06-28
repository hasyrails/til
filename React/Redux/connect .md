## connect 
### ```connect()()```の各引数の機能
> ```jsx
> connect(func1, func2)(Test);
> ```
> 第一引数の「func1」はcomponentに渡すpropsを制御する  
> 第二引数の「func2」はreducerを呼び出して、reduxで管理しているstateを更新する  
> Testは取得したデータをpropsとして扱いたいcomponentを指定する  

https://qiita.com/macotok/items/ddbebfbb7dd3d834d86e

### 実装例
```jsx
connect(
  mapStateProps,
  mapDispatchProps
)(Counter);
```

