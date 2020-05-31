## 重複を禁止するuniqueness

### （例）重複したメールアドレスのデータ登録を許さないバリデーションの設定
メールアドレスのレコードを格納するmailカラムに対して  
次のようにバリデーションを設定する。
```
validates :mail, uniqueness: true
```

### オプション case_sensitive

大文字・小文字を区別するかどうかを設定するには  
バリデーションオプション case_sensitive を用いる。

・```case_sensitive: true```    →　大文字・小文字を区別する  
　　→　hoge@example.com　と　Hoge@example.com　は違うメールアドレスと区別するので重複していない  
・```case_sensitive: false```   →　大文字・小文字を区別しない  
　　→　hoge@example.com　と　Hoge@example.com　は違うメールアドレスと区別しないので重複  

デフォルトは case_sensitive: true

```uniqueness: true```でかつ```case_sensitive```のオプション設定を使うときは次のように設定する
```
validates :mail, uniqueness: { case_sensitive: false } 
```
