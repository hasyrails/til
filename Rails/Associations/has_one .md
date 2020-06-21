## has_one

1 - 1 のアソシエーション 

https://sakurawi.hateblo.jp/entry/2017/10/03/has_one%E3%81%A8belongs_to%E3%81%AE%E9%81%95%E3%81%84

### belongs_to/has_oneの違い

> 自身が他のテーブルをたどるキーを所持している場合は、belongs_to  
> 自身が他のテーブルからたどるキーで示されている場合は、has_one

> ```
> class Supplier < ApplicationRecord
>   has_one :account
> end
> ```

> Supplierのテーブルにはaccountのidなどはもっていません。 しかし、Accountテーブルはsupplier_idのようにこちらを示すカラムがある場合です。
