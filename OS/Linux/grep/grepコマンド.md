## grepコマンド　-検索-

### grepってなんの略？
grep = **g**lobal **r**egular **e**xpression **p**rint
  
  global : ファイル全体から  
  regular expression :　正規表現による検索結果を  
  print :　表示する  

https://ja.wikipedia.org/wiki/Grep

な、なるほど

### grepコマンドの使い方

```
$ grep (検索ワード)　(絶対パス：どのディレクトリで検索するか)
```

（例） ディレクトリapp/controllers/user_sessions内で「log_in」というワードが使われているかを検索する

```
$ grep log_in app/controllers/user_sessions 
```
