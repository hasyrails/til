### LaTexで書いた数式をマークダウンで使用する方法
 LaTexで書いた数式をGitHubのマークダウンで使う場合のプロセスをメモ
 
 #### CODECOGS
  - [CODECOGS](https://www.codecogs.com/latex/eqneditor.php )に数式を入力する　
    - 入力した内容をLaTexでコンパイルした結果がプレビューされる
  - URL出力する
 #### マークダウン入力部
  - マークダウン入力フォームでCODECOGSで出力したURLをimgタグのパスとして画像出力する
    - <img src=[CODECOGS output URL] />

#### 参考
 - [GithubのREADMEとかwikiで数式を書く](http://idken.net/posts/2017-02-28-math_github/)
