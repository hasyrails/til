## ```belongs_to```
```has_one```と同じく、
1 - 1 のアソシエーション 

### ```has_one```/```belongs_to```の違い

> 自身が他のテーブルをたどるキーを所持している場合は、belongs_to
>
> ```ruby
> class Book < ApplicationRecord
>   belongs_to :author
> end
> ```
> と書くとすると Bookテーブルが、author_idをカラムに持っていてAuthorをたどれます。
