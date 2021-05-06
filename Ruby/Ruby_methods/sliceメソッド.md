## 文字列を切り取るsliceメソッド
``` ruby
# str : Stringクラスのオブジェクト 

str.slice(num1, num2)
# strのnum1文字目からnum2文字分を切り取る
```

例えば````str == "銀座Rails"```の場合
``` ruby
# str == "銀座Rails"

str.slice(3,4)
# => "Rail"
```

## 正式には
```slice```メソッドは配列に対して定義されている
https://docs.ruby-lang.org/ja/latest/method/Array/i/slice.html
``` ruby
Array.slice(num1, num2)
```

### Stringクラスオブジェクトは配列として扱える？
> じつは、RubyのStringクラスの文字列は、文字列を構成する文字ごとに要素番号が割り振られています。
https://web-camp.io/magazine/archives/16198

## URLの切り取りに便利
YouTube / Twitter の埋め込みなどに便利。
