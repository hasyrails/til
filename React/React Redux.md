## Reduxはreactだけのためのものではない
> Reduxとは  
> state（状態）を容易に管理をするためのフレームワークのこと。  
> Reactと相性が良いため、セットで紹介されていることが多いが、  　
> Redux自体は独立したものなので単体で利用することも可能。  

https://qiita.com/soarflat/items/bd319695d156654bbe86#redux%E3%81%A8%E3%81%AF

## reactへのインターフェース関数

### Provider
・公式より
>The <Provider /> makes the Redux store available to any nested components that have been wrapped in the connect() function.
>
> Since any React component in a React Redux app can be connected, most applications will render a <Provider> at the top level, with the entire app’s component tree inside of it.  
https://react-redux.js.org/api/provider#overview

・Qiita

> Providerの目的は2つ
> 1. Reactコンポーネント内でreact-reduxのconnect()関数を使えるようにすること
> 2. ラップしたコンポーネントにstore情報を渡すこと
> 
> 項目1についてはReactをそれなりにやっていると理解できると思いますが、  
> 項目2ですでに初見殺しだと思います。  
しょ、初見殺し‥
https://qiita.com/MegaBlackLabel/items/df868e734d199071b883

### connect

・公式より

> The connect() function connects a React component to a Redux store.
> 
> It provides its connected component with the pieces of the data it needs from the store, and the functions it can use to dispatch actions to the store.  
https://react-redux.js.org/api/connect#overview

・Qiita
> Reduxの「store」にReactがアクセスするための関数であり、そのユースケースがいっぱいあるよとあります。
https://qiita.com/MegaBlackLabel/items/df868e734d199071b883#connect
