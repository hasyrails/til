## コミットメッセージで改行を使いたい

### git commit -m で改行する

```
$ git commit -m '(コミットのメッセージ)'  
```
では、コミットメッセージが１行しか残せず、  
前のコミットに対して変更を複数加えた場合（コミット粒度が大きい場合）  
のちのち見づらくくなるだろうし、どうしようか、、、と思っていた

-m を複数回使うことで
改行することができる

（例）
```
$ git commit -m 'line1' -m 'line2' -m 'line3'
```
でコミットした時、
コミットメッセージは次のようになる。

```
commit 5d985c547055534b7a716cb4a105aeddcfe96482
Author: username <hogehoge@mailaddress.com>
Date:   Fri May 22 23:40:25 2020 +0900

    line1
    
    line2
    
    line3
```

改行に空白が入ってしまうのがデフォルトなので、  
空白行を入れる場所を自分で調整したい場合は  
ヒアドキュメントを用いてコミットメッセージを残すのが良い↓  

### ヒアドキュメントを使って改行する。

ヒアドキュメントを使ってコミットコメントを残すには次のコマンドを使う
```
# ヒアドキュメント識別子をEOM(End Of Message)とする 
$ git commit -F- <<EOM　
```
returnキーを押すと  
EOMを打つまでheredoc> で改行してくれる

```
$ git commit -F- <<EOM
heredoc> line1 #returnキーで次の行に改行　新しいheredoc>が出てくる 
heredoc> line2
heredoc> line３
heredoc> EOM　 #コメントを終了したい時はヒアドキュメント識別子を打ち込む
```
$git log で確認できるメッセージは次のようになる。

```
commit 4ea04ad919cb56ee3ec87796beaa268cf260394b
Author: username <hogehoge@mailaddress.com>
Date:   Sat May 23 00:23:57 2020 +0900

    line1
    line2
    line3

```

