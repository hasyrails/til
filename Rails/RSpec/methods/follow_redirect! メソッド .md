## follow_redirect!メソッド　- redirect_toを検証 -

> ### follow_redirect!メソッド
> Railsテスティングガイドによると、
> ```
> 単一のリダイレクトレスポンスに従う。
> ```
> とのこと。 チュートリアル内にも以下のように説明されている。
> ```
> POSTリクエストを送信した結果を見て、指定されたリダイレクト先に移動するメソッド
> ```
> つまり、follow_redirect!は、  
> assert_difference内で、users_pathへのPOSTリクエスト（URL：/users、アクション：create）を送信した  
> 結果（レスポンス）を見て、  
> controllerで指定しているリダイレクト先のuser_url @user（ユーザ登録完了後のユーザ画面）へ移動している。
> ```
>   test "valid signup information" do
>     get signup_path
>     assert_difference 'User.count', 1 do
>       post users_path, params: { user: { name:  "Example User",
>                                          email: "user@example.com",
>                                          password:              "password",
>                                          password_confirmation: "password" } }
>     end
>     follow_redirect!
> 
>   def create
>     ・・・略・・・
>     if @user.save
>       #保存の成功をここで扱う
>       flash[:success] = "Welcome to the Sample App!"
>       redirect_to user_url @user
> ```
> そのため、follow_redirect!の後、  
> 特定のユーザを表示するページ（URL: /users/ユーザID）が表示されることを期待して、  
> users/showテンプレートのテストを行っている。  
> ```
>  test "valid signup information" do
>　　・・・略・・・
>    follow_redirect!
>    assert_template 'users/show'
>  end
> ```
> Userのルーティング、Userのshowアクション、show.html.erbビューが  
> それぞれ正常に動いているかをテストすることができる。

引用：https://www.yokoyan.net/entry/2017/05/03/000000
