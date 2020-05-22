### mkdirコマンドのオプション

#### -p オプション

-p = --parents (親ディレクトリを作成する)

##### mkdirコマンドは作成したいディレクトリまでのディレクトリパスが存在していることが前提
```
# ディレクトリ /parent は存在しないとする

$ mkdir /parent/child/grandchild
# エラーでgrandchildディレクトリは作成できない
```

parentディレクトリが存在しない状況で、
次のようなコマンドでgrandchildディレクトリを作成しようとするとエラーとなる。

##### -pオプションを使うとディレクトリパスを作ってくれる
```
# ディレクトリ /parent は存在しないとする

$ mkdir　-p /parent/child/grandchild
# 作成したいgrandchildディレクトリまでのパス　/parent/childディレクトリも自動的に作成（便利）
```

