## エラーの配列を出力する　- errorsメソッド -  

### Rails標準のメソッド

Rails標準のメソッド。
rails cでバリデーションの有効性を調べたりで使える

> ```Ruby
> class Person < ApplicationRecord
>   validates :name, presence: true
> end
>  
> >> Person.new.errors[:name].any? # => false
> >> Person.create.errors[:name].any? # => true
> ```
> https://railsguides.jp/active_record_validations.html#%E3%83%90%E3%83%AA%E3%83%87%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%AE%E6%A6%82%E8%A6%81-errors

### valid? / invalid? メソッドとは検証範囲が違うことが注意

#### valid?メソッドでの検証

```Ruby
Person.create(name: "John Doe").valid? # => true or false
Person.create(name: nil).valid? # => true or false
```
https://railsguides.jp/active_record_validations.html#valid-questionmark%E3%81%A8invalid-questionmark

これは、validメソッドで属性```name```について検証しているように見えるがそうではない。

> ```Ruby
> # Personテーブルカラム　name, age, gender, emailとする
> 
> Person.create(name: "John Doe", age: 23).valid? # => true or false
> # Person.create(name: "John Doe", age: 23, gender: nil, email: nil)を検証する
> # 値を指定していない属性も補完してオブジェクト全ての属性に対して検証している 
> ```

オブジェクト **全体（全ての属性)** を検証するのが valid? / invalid? メソッド

#### errors[]メソッドでの検証
> ```Ruby
> >> Person.new.errors[:name].any? # => false
> >> Person.create.errors[:name].any? # => true
> ```

オブジェクトの **指定した属性のみ** を検証するのが  メソッド

https://railsguides.jp/active_record_validations.html#valid-questionmark%E3%81%A8invalid-questionmark

### RSpecのバリデーションエラーメッセージの検証に使ったので

```Ruby
expect(@task.errors[:status]).to include("can't be blank")
```

・ ```@task.errors```　：```@task```のエラーメッセージに対する配列  
・ ```@task.errors[:status]```　：```@task```の属性```status```についてエラーメッセージのみを取り出した配列  
