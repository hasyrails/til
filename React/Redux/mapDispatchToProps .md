## DispatchをToProps - mapDispatchToProps -

> ## mapDispatchToProps
> →「Dispatch（Action関数）」を「ToProps」  
> 　Action関数をPropsとして扱うことができるということ。  

## mapDispatchToPropsはAction呼び出しコール
> ボタンコンポーネントの孫コンポーネントがあったとしましょう。  
> 本来なら孫コンポーネントからはアクション関数を呼び出すことはできません。  
> 親→子→孫と繋いでようやくクリックの挙動が発動されます。  
> ですが、  
> この「mapDispatchToProps」を使うとこれも親や子なんかお構いなし！  
> 孫コンポーネントから即呼びできるようになります。こんな感じです。  
> ``` jsx
> import { actionA } from './actionCreator'
> import { bindActionCreators } from 'redux'
> 
> const mapDispatchToProps = dispatch => {
>   return bindActionCreators({ actionA }, dispatch)
> }
> ```
> 孫コンポーネントさんがアクションAさんを使いたいと
>「mapDispatchToProps」を使ってアクションAさんを直接呼び出しています。（Propsに追加しています）
