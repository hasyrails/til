## uuid is 何

> UUIDとはUniversally Unique Identifierの略。
> 普遍的にユニークなIDということです。
> 誰でも作れて世界中で被らないたった一つのIDと言えます。
> こんな感じです→例：550e8400-e29b-41d4-a716-446655440000

https://qiita.com/bSRATulen2N90kL/items/a26f5a1edf4f69a51f62

## uuidを使う意味

### デフォルトのidだとセキュリティが‥

> ユーザーidなどのIDが順番に取得されているので、  
> 例えば下記のルートのように、 https://hogu.com/user/5  
> とか適当に手入力するとページ上からアクセスしなくても画面遷移してしまう。  

https://qiita.com/params_bird/items/9e162fdcd9bdc2e42ccd

> 知り合いの凄腕エンジニアに聞いたんだけど、  
> /users/32ってURLにユーザー数が丸見えになってるって、このセキュリティーは流石にまずいよ、駒形さん  

https://docs.komagata.org/5455

## uuidの設定
```user```の```id```を```uuid```化する

```string```型の```uuid```カラムを設定
```ruby
create_table "users" do |t|
    t.string "uuid"
```

```ruby
class User < ApplicationRecord
  before_create -> { self.uuid = SecureRandom.uuid }
end
```


