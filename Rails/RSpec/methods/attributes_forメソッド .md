## attributes_forメソッド - ファクトリデータの属性値をハッシュで取得する

buildはモデルオブジェクト、attributes_forはハッシュを取得する
> buildとattributes_forで取得するデータの違いが以下の通りです。
> 
> build
> ```
> > FactoryBot.build(:post)
> => #<Post id: nil, content: "test content", user_id: 8, created_at: nil, updated_at: nil> 
> ```
> attributes_for
> ```
> > FactoryBot.attributes_for(:post)
> => {:name=>"test", :email=>"test2@test.com", :password=>"password"}  
> ```
>buildはモデルオブジェクト、attributes_forはハッシュとなっていますね。

https://qiita.com/__kotaro_/items/adbc355bfb550b8b2150

## 実際にやってみた

### taskファクトリの定義
```
FactoryBot.define do
  factory :task, class: Task do
    title { 'ランニング' }
    content { 'A公園' }
    status { 0 }
    deadline { '2020-6-20 7:00' }
    
    association :user,
      factory: :user,
      email: 'test1@example.com'
    end
end
```

### buildメソッド
```
> FactoryBot.build(:task)
=> #<Task:0x00007facae44dfd8
 id: nil,
 title: "ランニング",
 content: "A公園",
 status: "todo",
 deadline: Sat, 20 Jun 2020 07:00:00 UTC +00:00,
 created_at: nil,
 updated_at: nil,
 user_id: nil>
```

### attributes_forメソッド
```
> FactoryBot.attributes_for(:task)
=> {:title=>"ランニング", :content=>"A公園", :status=>0, :deadline=>"2020-6-20 7:00"}
```
id、timestamp、アソシエーションを除いた  
tasksテーブル作成で作ったカラムに対応する属性値をハッシュとして取得できる

### ハッシュが欲しい時の王道パターン：ログイン

```
post "/login", params: { user: FactoryBot.attributes_for(:user) }
```
