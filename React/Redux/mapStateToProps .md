## 公式
https://react-redux.js.org/using-react-redux/connect-mapstate#connect-extracting-data-with-mapstatetoprops

## 参考
[mapStateToPropsとmapDispatchToPropsの理解の仕方](https://ocws.jp/blog/post1866/)

### Propとは
>「mapStateToProps」と「mapDispatchToProps」はどっちも名前の通り、「ToProps」なんです。  
>つまり、Propsにする（変換する・適応する）ってことです。  
>つまり、  
>***Propsとして使うことができるようにする***ということなんですね。  

> ## mapStateToProps  
> →「State」を「ToProps」  
> 　State情報をPropsとして扱うことができるということ。  

### mapStateToPropsはPropsエントリーチケット
> 子コンポーネントでStateの情報を使いたいとき、
> 本来なら親コンポーネントからPropsとして引き継いでもらわないといけないんですけど、
> 「mapStateToProps」を使うとそんなことはお構いなしに親コンポーネントから引き継がなくても
> 子コンポーネントからすぐに使うことができるようになります。
> ``` jsx
> const mapStateToProps = state => {
>  return { cprops: state.cprops }
> }
> ```
> 「mapStateToProps」という“チケット”を持っているC Propsくんは見事Propsとして入ることができるんですね。
