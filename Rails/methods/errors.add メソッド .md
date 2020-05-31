## errors.addとは

カスタムメソッドを  
バリデーションメソッドとして設定したとき  
エラーメッセージを表示させるのに用いる  
（用いたので備忘録。）

## カスタムメソッドをバリデーションメソッドとして設定する方法

```validate :(CustomMethodName)```とセット  
  
例↓

```
class HogeProject < ApplicationRecord

  validates :name, presence: true, length: { maximum: 200 } 
  # テーブルのカラムに対するバリデーションには validates で表す
  ・
  ・
  ・
  validate :has_options?
  # カスタムメソッドをバリデーションメソッドとして設定する時は validate で表す

  def has_options?
    errors.add(:options, "を選んでください") if self.options.blank?
  end

end

```

## 参考
https://qiita.com/yujiG/items/3e34e2e0e7b4120b0584
https://qiita.com/yusaku_/items/b84d4fd2d6d5b4ee22c5
