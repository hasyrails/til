## 認可システム -pundit-
### 認可システムgem - punditとcancancan -
> Punditというgemを使ってRailsに認可の仕組みを作ってみます。認可というとcancancanが有名です。  
> cancancanはユーザに対して、どんなアクションが許可するかを定義するのに対して、Punditではリソースに対して誰が許可されるのかを定義します。  
> 反対からの目線ですね。cancancanがコントローラ寄りならば、Punditはモデル寄りの責務です。  
> また、cancancanがDSLなのに対し、PunditはピュアRubyな書き方になっています。
https://qiita.com/zaru/items/8bf7b41b33f3f55bd27d

### ちな
pundit: 賢者、学者

## ```authorize```メソッド
```gem 'pundit'```のカスタムメソッド  
公式wikiより
> ```ruby
> def update
>   @post = Post.find(params[:id])
>  authorize @post
>  if @post.update(post_params)
>    redirect_to @post
>  else
>    render :edit
>  end
> end
> ```
> The authorize method automatically infers that Post will have a matching PostPolicy class,  
> and instantiates this class, handing in the current user and the given record. 

### PostPolicyクラス？？
> ```ruby
> unless PostPolicy.new(current_user, @post).update?
>   raise Pundit::NotAuthorizedError, "not allowed to update? this #{@post.inspect}"
> end
> ```

```PostPolicy```クラスに属していないレコードを更新しようとする場合、
```Pundit::NotAuthorizedError```が発生するように定義している。

```authorize```メソッドで```PostPolicy```クラスに属させることを宣言している
