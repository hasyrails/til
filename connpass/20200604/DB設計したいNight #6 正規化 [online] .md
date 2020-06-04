## アンケート、申込フォーム用のデータベース作成

・途中から参加

・入力項目に対応するテーブルカラムが多岐にわたるようになり、整合性が取れなくなる

解決策として  
・RDBにしない？  
・JSONを使う？  
・見た目とDB設計は別で考える　　

## Nullを避けるデータベース設計

・ORDER_BYに対する挙動  
　・PostgreSQL ではNullが最後になる  
　・MySQL ではNullが最初になる  

・NULL撲滅委員会　　

・バリデーションをスキップする（すり抜ける）場合がある？？  
　・update_allメソッド  
  ・全てのカラムにnullを入れないように設計する  
  
・null-freeなデータベース設計  
　・できるだけNOT NULL制約をつける  
　・テーブルを分ける  
　・モデルを分ける  
　・パフォーマンスが悪くなってからスターテスを追加する  

・ActiveRecord v6.1 の新機能  
  ・where.missing(:author)  
  ・check_contraint  
 
・テーブルを状態で分ける  
　・記事公開/非公開  
　・タスクの完了/未完了  
 
 ・json型、jsonで保存？？  
 　・jsonで:user_archiveカラムを残しておいて:userは残す？？  
 　
 ・Generated Column?? jsonにインデックスを貼れる？？  
 
 
