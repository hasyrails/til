## ```rails db:rollback``` -migrationを取り消す-

### 基本は１つずつ戻る
```
$ rails db:rollback
```
でmigrationを１つ戻せる

### ```STEP=N```で複数回分戻せる
```
$ rails db:rollback　STEP=N
```
でN個分のmigrationを戻せる

### 備忘録
```step=N```と小文字でコマンド出しても反応せず、１つしか戻らなかった
