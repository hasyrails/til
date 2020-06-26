## レコードの状態を定義する -```enum```メソッド- 

### Rails標準のメソッド
gemのインストールは不要

> 「Enum」は「列挙型」のこと。  
> この列挙型を扱う機能としてRuby on Rails4.1からActiveRecord :: Enumと言うモジュールが追加となりました。  
https://qiita.com/ozackiee/items/17b91e26fad58e147f2e  

### enumで定義した状態を条件式に使いたい場合

#### 実装例
記事```article```のステータス```state```によって表示するフラッシュメッセージを変える  
・記事編集画面から「更新する」を押した際に、  ステータスが「下書き状態以外」かつ、公開日時が「未来の日付」に設定された場合  
 --> ステータスを「公開待ち」に変更して「更新しました」とフラッシュメッセージを表示  
・記事編集画面から「更新する」を押した際に、  ステータスが「下書き状態以外」かつ、公開日時が「現在または過去の日付」に設定された場合  
--> ステータスを「公開」に変更して「更新しました」とフラッシュメッセージを表示  

``` ruby
class Article
  enum state: { draft: 0, published: 1, publish_wait: 2 } 
end
```

```update```メソッド
```ruby
class ArticlesController < ApplicationController
  def update
    if @article ~~~ #== Articleの状態による条件分岐 ==
  end
end
```

#### enumで定義した状態を呼び出す
enumで定義した状態＋？　で状態をtrue/falseで判定することができる
```
> article = Article.new(state: :draft)
> article.draft?
=> true
> article.published?
=> false
```
```ruby
if @article.draft?　#== @articleがdraft(下書き)の状態の場合 ==
```
