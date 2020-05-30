## ja.ymlに過剰な設定で怒られた件

### エラー
https://gyazo.com/14f3b49dba45837af31ba8cd5a0c70c4

### 設定
クラス変数@@foodsでja.ymlの辞書データの呼び出し(.human_attribute_name)を定義 
```
@@foods = [
   {
     id: 0,
     name: FoodEnquete.human_attribute_name(:food_list)[0][:name]
   },
   {
     id: 1,
     name: FoodEnquete.human_attribute_name(:food_list)[1][:name]
   },
   {
     id: 0,
     name: FoodEnquete.human_attribute_name(:food_list)[2][:name]
   }
 ]
```

ja.ymlで辞書データの設定

```
ja:
  activerecord:
    models:
      food_enquete: お食事についてのアンケート
    attributes:
      food_enquete:
        food_id: ご注文した料理
        food_list:
          - name: ラーメン
          - name: カレー
          - name: 焼きそば

```
### エラー原因、解消

クラス変数@@foodsの```name:```の設定を変更
```
# ja.ymlの配列food_listから選ぶ設定を変更
@@foods = [
   {
     id: 0,
     name: FoodEnquete.human_attribute_name(:food_list)[0]　#[:name]を消去
   },
   {
     id: 1,
     name: FoodEnquete.human_attribute_name(:food_list)[1]　#[:name]を消去
   },
   {
     id: 0,
     name: FoodEnquete.human_attribute_name(:food_list)[2]　#[:name]を消去
   }
 ]
```

ja.ymlの設定を変更
```
ja:
  activerecord:
    models:
      food_enquete: お食事についてのアンケート
    attributes:
      food_enquete:
        food_id: ご注文した料理
        food_list:
        - ラーメン  #name:と指定していたのを変更
        - カレー　　#name:と指定していたのを変更
        - 焼きそば　#name:と指定していたのを変更
```

### まとめ

エラーが出た時の```:name```を使ったja.ymlの設定は、  
下記のように一つの要素の中に2項目ある時に必要

```
ja:
  activerecord:
    models:
      food_enquete: お食事についてのアンケート
    attributes:
      food_enquete:
        food_id: ご注文した料理
        food_list:
          - name: ラーメン
            price: 500
          - name: カレー
            price: 500
          - name: やきそば
            price: 300
```

[[name[0],price[0]],[name[1],price[1]],[name[2],price[2]]]のような形？  
（要確認：データ型がどうなっているかja.ymlとの対応）

今回はnameの名前の辞書対応のみなのにわざわざ```name:```で指定したから怒られた

