## anyメソッド　とは

> any?メソッドは配列の要素を1つずつ評価し、ブロックに記述した条件が真になったらtrueを返すメソッドです。

> 書き方： ```オブジェクト.any? { |要素| ブロック処理}```

https://www.sejuku.net/blog/58980

## 例

クラス変数@@presentsを次のようなハッシュ（連想配列）で定義したとする。
```
@@presents = [
{
  id: 0
  adult_only: true 
},
{
  id: 1
  adult_only: false
}
：
]
#id, adult_only というkeyを持つハッシュ
```

次のような条件を考えてみよう。
```
@@presents.any? { |present| present[:id] == present_id && present[:adult_only] == true }

# present[:id] = present_id     : @@presentのハッシュ要素のうち、キーidがpresent_id(テーブルのレコードのid値)に等しいもの
# present[:adult_only] = true   : @@presentのハッシュ要素のうち、キーadult_onlyがtrueであるもの
```

