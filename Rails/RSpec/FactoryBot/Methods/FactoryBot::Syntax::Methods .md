## FactoryBot::Syntax::Methods -FactoryBotのコードを簡略化-

helper/rails_helper で下記のように設定する
```ruby:rails_helper.rb  
RSpec.configure do |config|
  config.include FactoryBot::Syntax::Methods

end
```

これにより、
> FactoryBot シンタックスを省略できます．

> ```ruby
> # before
> FactoryBot.build(:user)
> FactoryBot.create(:user)
> FactoryBot.build_stubbed(:user)
> FactoryBot.attributes_for(:user)
> 
> # after
> build(:user)
> create(:user)
> build_stubbed(:user)
> attributes_for(:user)
> ```

引用：http://yurafuca.hatenablog.com/entry/2018/06/28/190842
