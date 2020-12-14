### scaffoldでモデル作成
``` 
$ rails g scaffold [model name] [column1 name]:[column1 data type] [column2 name]:[column2 data type]
```

### Rails MVC でのコードの呼ばれ方

C(Controller) →　M(Model)　→ V(View)

（例）User一覧画面

- (1) Controllerでアクションが呼ばれる
- (2) アクション内でモデルを参照する
``` ruby
# app/controller/users_controller.rb

class UsersController < ApplicationController
  def index
    @users = User.all
  end
end
```

- (3)モデルが呼び出される
``` ruby
# app/models/users.rb

class User < ApplicationRecord
end
```

- (4)変数をViewに表示させる
``` ruby
# app/view/users/index.html.erb

...
<%= link_to 'New User', new_user_path %>
```

ビューでヘルパーメソッドを使うことでモデルの情報をビュー内で扱うことができる

