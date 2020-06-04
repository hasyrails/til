## empty?メソッド

### 公式Railsドキュメント
> empty?
> ```
> 変数.empty?
> ```
> Rubyの標準メソッド。空の文字列や空の配列の場合にtrueを返す。  
> nilに対して呼び出すとNoMethodErrorが発生

https://railsdoc.com/active_support

### 入れ物があることが前提
公式ドキュメントの

> nilに対して呼び出すとNoMethodErrorが発生　　

の記述に関して

> ```
> book.empty?
> description.empty?
> ```
> は、bookやdescriptionそのものは存在していることが前提で、  
> その配列の中身が空か、文字列の中身が空の場合にtrueを返す。  
> 配列や文字列そのもの（入れ物）が無い場合にはNoMethodErrorが発生する。  
> 空ですか？と聞いてるわけだから、少なくとも「入れ物」が存在しないとダメってことか。  

https://qiita.com/somewhatgood@github/items/b74107480ee3821784e6
