## コミット内容をわかりやすく
git log で過去のコミットがどのような内容なのかわからない
→ git commit のメッセージでprefix をつける。

#### 参考
https://qiita.com/numanomanu/items/45dd285b286a1f7280ed


## prefixのパターン①
prefix のパターン  
  ・feat     :　新機能追加  
  ・fix      :　バグの修正  
  ・docs     :　documentの修正のみ  
  ・style    :　コードの意味に影響を与えない部分の修正(空白スペース、セミコロン抜けの修正など)  
  ・refactor :　featでもfixでもない修正  
  ・perf     :  パフォーマンスを上げるためのコード修正  
  ・test     :　テストコードの修正  
  ・chore    :　ビルドプロセスの変更、補助ツール、ライブラリの変更など  

#### 参考
https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#type

## prefixのパターン②　（2020/05/23追記）
こちらのQiita：　https://qiita.com/itosho/items/9565c6ad2ffc24c09364
で紹介されている「ライト版」を今後使用しようか検討
(先述のprefixの種類を忘れてしまう)

prefix のパターン    
  ・fix : バグ修正
  ・add : 新規ファイル追加/新規機能追加
  ・update : 機能修正（バグ修正ではない修正）
  ・remove : ファイル削除

## Rails開発をするのであればやはりパターン①か

パターン①は数が多くて覚えきれないという欠点があるが
Robocupで指摘されるエラー修正と対応を付けやすい利点が大きいのが現時点（２０２０/05/23）での見解。
