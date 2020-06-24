## 初期データの設定に ```gem `seed-fu` ```

```ruby
gem 'seed-fu'
```
が初期データの設定にいいらしい

### ```rails db:seed``` より初期データの設定がしやすい？
> Railsアプリを作るときに、変更する機会が少ない初期データは、  
> rake db:seed で読み込ませるのが良さそう・・・な気がした。  
> が、細かい設定がしづらい。  
https://qiita.com/m-shin/items/0a0848ef1f5d46df745d

### ほぉ

> Railsにはデフォルトで初期データを入れる仕組みとして rake db:seed がありますが、　　
> これは実行する度に同じデータが作成されてしまいます。　　
> そこで、代わりにseed-fuを利用するとデータの追加、管理が簡単にできるようになります！　　
https://remonote.jp/rails-seed-fu

## SeedFu.seed とは
```ruby
SeedFu.seed
```
はソースコード内で定義されている。

> SeedFu.seedはSeedRu::Runner#runを実行します  
https://blog.freedom-man.com/seed-fu-codereading
