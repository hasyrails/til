## iキーでINSERTモードへ移行

### ①vimを起動
```
$ vim [file]
```

### ②iキーを押すとINSERTモードとなる

iキーを押すとINSERTモードになる　（-- INSERT -- と表示される）

```
class UserSessionsController < ApplicationController
  skip_before_action :require_login, only: %i[new create]
：
：
end
~
：
~                                                                                                    
-- INSERT --
```

ファイル内容編集可能となる


