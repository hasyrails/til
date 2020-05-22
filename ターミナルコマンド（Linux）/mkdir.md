## mkdirコマンド　-ディレクトリ作成-

mkdir = **m**a**k**e **dir**ectory

### カレントディレクトリでディレクトリを新規作成

```
# カレントディレクトリ ExampleApp 
$ mkdir hoge_directory
```
→　ディレクトリ ExampleApp/hoge_directrory が作成される

### 絶対パスを指定してディレクトリを新規作成

```
# カレントディレクトリ ExampleApp 
$ mkdir /app/fuga_directory
```

→　ディレクトリ　/app/fuga_directory が作成される  
   （カレントディレクトリがどこかは関係ない）

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

