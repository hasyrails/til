## shared_exampleメソッド -一度定義したら他のテストケースで使い回せる-  

> shared_examplesは下記のような感じで共通化したいexampleを記載します。
> ```
> shared_example "exampleのタイトル" do
>   expect(...)
> end
> ```

> 定義したshared examplesは、下記のように呼び出して使います。  
> ```
> describe Model do  
>　 　# shared_exampleをincludeする  
> 　　include_examples "#{exampleのタイトル}"  
> 　　　context 'こんな場合' do  
> 　　　　# shared_exampleで定義した結果と同じになるとテストがgreenになる  
> 　　　　it_behaves_like "#{exampleのタイトル}"  
> 　　　end  
> end  
> ```
参考：https://qiita.com/yu-croco/items/d0088a75b033d46f8c39
