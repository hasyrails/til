## "FactoryBot"を省略してメソッドを使えるように
> ```
> RSpec.configure do |config|
>   config.include FactoryBot::Syntax::Methods
> end
> ```

https://qiita.com/jonakp/items/0f70eece4fe7980f81a6

### 公式READ ME
> If you do not include FactoryBot::Syntax::Methods in your test suite, 
> then all factory_bot methods will need to be prefaced with FactoryBot.

https://www.rubydoc.info/gems/factory_bot/file/GETTING_STARTED.md

### 例

```
user = FactoryBot.build(:user)
```
↓ FactoryBotを省略
```
user = build(:user)
```
