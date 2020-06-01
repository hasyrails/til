## letメソッド - インスタンス変数/ローカス変数の生成を記述する -

### letメソッドの使用例

例として次のようなテストケースを行いたいとする。
```
describe 'セッション機能' do
  it 'ログインできること' do
  　new_user = User.new
    ‥‥
  end
  
  it 'ログアウトできること' do
  　new_user = User.new
   ‥‥
  end
end
```

ローカル変数```new_user```の生成
```
new_user = User.new
```
が重複している。

```
let(:new_user) { User.new }
```
でリファクタリングできる。

```
describe 'セッション機能' do
+ let(:new_user) { User.new }
  it 'ログインできること' do
  　- new_user = User.new
    ‥‥
  end
  
  it 'ログアウトできること' do
  　- new_user = User.new
   ‥‥
  end
end
```


### letメソッドはdescribeブロック内で使う
> let は、RSpec の describe ブロックの中で「メモ化されたヘルパーメソッド（memoized helper method）」を定義するメソッドです。

引用：https://www.oiax.jp/rails/rspec_capybara_primer/let_and_factory_girl.html
