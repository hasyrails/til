## ActiveStorage用のGem
Rails６に実装されているGem  

Rails５で使用できる```gem 'mini_magick'``` の画像変換機能  
Rails6から使用できる```Vips```の画像変換機能  
を```variant```メソッドで使うことができる  
https://railsguides.jp/active_storage_overview.html#%E7%94%BB%E5%83%8F%E3%82%92%E5%A4%89%E6%8F%9B%E3%81%99%E3%82%8B

> ```
> <%= image_tag user.avatar.variant(resize: "100x100") %>
> ```
↑
```resize```は
```gem 'mini_magick'```で定義されている画像変換オプション

画像変換のメソッドを定義して、  
なおかつview側で  
```variant```メソッドによる画像変換オプションの呼び出しをしたい時に使う。
