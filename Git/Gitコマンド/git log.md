### git log : コミットの履歴を確認する
```
$ git log
```
コミットの履歴一覧を表示する

#### git log の使用例
```
$ git log

commit 3e901b33f0c22d63fe239c1f9d89d989c440aafa (HEAD -> 63_flash_message)
Author: hasyrails <hasyrails@gmail.com>
Date:   Tue Mar 30 06:56:40 2021 +0900

    フラッシュメッセージのパーシャルを作成

commit e6e5224448472bdb0fbd8fc8510d2cf53dd4445e (origin/master, master)
Merge: 880d8c4 73b635b
Author: hasyrails <62625114+hasyrails@users.noreply.github.com>
Date:   Mon Mar 29 01:37:18 2021 +0900

    Merge pull request #195 from hasyrails/62_uuid
    
    62 uuid / uuid化
```
一覧が表示されるが、内容は表示されない

### git log -p -n : n個前までのコミット詳細を確認する (n=1,2,3...)

#### git log -p -1の使用例
```
$ git log -p -1
commit 3e901b33f0c22d63fe239c1f9d89d989c440aafa (HEAD -> 63_flash_message)
Author: hasyrails <hasyrails@gmail.com>
Date:   Tue Mar 30 06:56:40 2021 +0900

    フラッシュメッセージのパーシャルを作成

diff --git a/app/javascript/stylesheets/application.scss b/app/javascript/stylesheets/application.scss
index c2858ec..af06b84 100644
--- a/app/javascript/stylesheets/application.scss
+++ b/app/javascript/stylesheets/application.scss
@@ -71,3 +71,18 @@ a{
   text-decoration: none;
   color: grey ;
 }
+
+.notification {
+  z-index: 100;
+  .notice {
+    background-color: #DDFFFF;
+    color: grey;
+    text-align: center;
+    font-size: 16px;
+  }
+  .alert {
+    background-color:  palevioletred;
+    color: grey;
+    text-align: center;
+  }
+ }
diff --git a/app/views/layouts/_flash_message.html.erb b/app/views/layouts/_flash_message.html.erb
new file mode 100644
index 0000000..98aee80
--- /dev/null
+++ b/app/views/layouts/_flash_message.html.erb
@@ -0,0 +1,8 @@
+<div
+class="notification"
+>
+  <% flash.each do |key, value| %>
+    <%= content_tag :div, value.html_safe, class: key %>
+  <% end %>
+</div>
+
```
