## ```rails db:rollback``` -migrationを取り消す-

### 基本は１つずつ戻る
```
$ rails db:rollback
```
でmigrationを１つ戻せる

### ```step=N```で複数回分戻せる
```
$ rails db:rollback　step=N
```
でN個分のmigrationを戻せる
