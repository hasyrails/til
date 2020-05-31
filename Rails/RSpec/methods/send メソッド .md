## sendメソッド -プライベートメソッドを呼び出す-

テストケース内でプライベートメソッドを使いたい時

> obj.send(:method)を使います。
> ```
> expect(obj.send(:private_method)).to ...
> ```

> 引数を渡す場合は、sendメソッドの第二引数以降に渡したい引数をつけます。
> ```
> expect(obj.send(:private_method, ref1, ref2, ...)).to ...
> ```
引用：https://dev.classmethod.jp/articles/rspec-recipe/
