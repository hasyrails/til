ActiveRecord とは

データベースのカラムを設定する手順のみで
データベースの要素を呼び出すメソッドを定義してくれる
Railsに内蔵された機能

カラム名と同様のメソッドを
インスタンスメソッドとして組み込んでくれる

ex)
Userモデル 
usersテーブルのカラム「name」を作った
→ .nameメソッドがActiveRecordによって作られる
　 
データベースの要素を呼び出すメソッド(SQL文で構成されているメソッド)は
ActiveRecord::Base　に定義されている
（ApplicationRecordのスーパークラス）

(モデル) < ApplicationRecord < Activerecord::Base
