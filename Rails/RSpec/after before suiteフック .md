## フック(hook)　-テストケースの前処理・後処理を記述する-
・```before```フック  
・```after```フック  
・```suite```フック  

> Rspecのconfigurationに記述する。
らしい。
https://qiita.com/syunk38/items/e6cc1282c5479555f748

### 例
```ruby
# == spec/spec_helper.rb ==
config.before :suite do
  SeedFu.seed
end
```
