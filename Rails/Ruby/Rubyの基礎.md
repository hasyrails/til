### オブジェクト(Object)
Ruby,はたまたRailsは万物がオブジェクト

### クラス(class)
オブジェクトの機能を決めるもの

### インスタンス
クラスに含まれる要素のこと

### メソッド
オブジェクトに動作をさせる

### 変数の区分
 - ローカル変数 : あるメソッド内でしか使用することができない変数
 - インスタンス変数 : オブジェクト全体が使用することができる変数
 
### 属性
オブジェクトが抱えるデータ

### 配列(Array)
[el(1), el(2), .. , el(n)]

### ハッシュ(Hash)
{ :key(1) => value(1), :key(2) => value(2), ... , :key(n) => value(n) }

様々な表記法がある
{ key(1): value(1), key(2): value(2), ... , key(n): value(n) }

### privateメソッド
メソッドを外部から利用できなくする

### Rubyっぽい書き方
#### nilガード
nilを返さないようにする
``` ruby
def children
  @children ||= []
end
```

chidren がnilの場合でも```[]```を返すようになる。

以下と同義
``` ruby
def children
  @children || (@children = [])
end
```

#### ぼっち演算子 ```&.```
ぼっち演算子は```&.```がひとりぼっちで絵をかく様に見えることから。
演算子の意味とは関係がない

正式名称はsafe navigation operator
メソッドのレシーバがnilの場合もエラーを返さなくなる

##### %記法
配列を作ることができる

 - %w : 全ての要素が文字列の配列を返す
``` ruby
%w(el(1), el(2), .., el(n))
# => [el(1).to_s, el(2).to_s, ..., el(n).to_s]
```

``` ruby
 > arr1 = %w(apple, banana, meron)
 > p arr1
 => ['apple', 'banana', 'meron']
 ```
 
  - %i : 全ての要素がシンボルの配列を返す
 
 ``` ruby
%w(el(1), el(2), .., el(n))
# => [el(1).to_sym, el(2).to_sym, ..., el(n).to_sym]
```

``` ruby
 > arr1 = %w(apple, banana, meron)
 > p arr1
 => [:apple, :banana, :meron]
 ```

#### 配列の各要素から特定の属性のみを取り出す
 - ```<<```を使う 
 - ```.map```メソッドを使う
 
 一番簡潔
 ``` ruby
 users = [user1, user2, user3]
 names = users.map(&:name)
 ```
 
