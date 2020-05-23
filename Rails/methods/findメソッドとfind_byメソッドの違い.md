## findメソッドとfind_byメソッドの違い
|メソッド|検索条件|検索対象が見つからない場合|
|:---|:---|:---|
|find|id|ActiveRecord::RecordNotFound|
|find_by|id以外のカラム（idでも検索可）|nil|

### 検索対象が見当たらない場合の挙動の違いを見て

findメソッドで発生するエラーは
「ActiveRecord::RecordNotFound」

```
# Userモデルにid=3のuserレコードが存在しないとき

User.find(3)
# →　ActiveRecordNotFound が発生する
```

「例外処理しないとアプリケーション落ちる」　→　カスタムメソッドでfindを使っている時、要留意
