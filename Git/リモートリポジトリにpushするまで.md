## リモートリポジトリへpushする

初push記念（2020/05/23）の備忘録  
Railsプロジェクトをpushしたのでrails new から  

### ローカルでコミット作成するまで
  ①ターミナル）Railsの環境設定（省略）  
  ②ターミナル）Railsプロジェクトのローカルリポジトリを作成  
  ```
  $ rails _rails-version_ new (LocalRepositoryName)
  ```
  ③Github)リモートリポジトリを作成する   
  ④Github)作成したリモートリポジトリのURLをコピー  
  ⑤ターミナル）リモートリポジトリURLを登録する
  ```
  # @ローカルリポジトリのトップ
  $ git remote　add <RemoteRepositoryName> <RemoteRepositoryURL> 
  ```
  ⑥ターミナル）ローカルリポジトリを登録したリモートリポジトリへpushする
  ```
  git push <RemoteRepositoryName> <LocalRepositoryName>
  ```
  ※メモ  
   リモートリポジトリとローカルリポジトリの順序は  
   英語文法のSVO1O2の順　（O1にO2を）  
  
### 参考
https://qiita.com/Futo_Horio/items/4d669f695680bc13d5fa
