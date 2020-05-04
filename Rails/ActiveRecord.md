<h1>ActiveRecord とは</h1>

データベースのカラムを設定する手順のみで
データベースの要素を呼び出すメソッドを定義してくれる
Railsに内蔵された機能

カラム名と同様のメソッドを
インスタンスメソッドとして組み込んでくれる

<p>ex)</p>
<p>Userモデル</p> 
<p>usersテーブルのカラム「name」を作った</p>
<p>→ .nameメソッドがActiveRecordによって作られる</p>
　 
<p>データベースの要素を呼び出すメソッド(SQL文で構成されているメソッド)は</p>
<p>ActiveRecord::Base　に定義されている</p>
<p>（ApplicationRecordのスーパークラス）</p>

<p>(モデル) < ApplicationRecord < Activerecord::Base</p>
