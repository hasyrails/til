## grepコマンド） -rオプション　-再帰的検索- 

```
$ grep -r search-string [dir | file]

# [dir | file] : dirctory OR file (|はOR)
```
参考 : https://tadtadya.com/linux-command-grep-search-the-file-recursively/

[dir|file]で指定したディレクトリ/ファイル配下のサブディレクトリ/サブファイルでも
search-string を再帰的に検索する

### 全体検索

(例)error_404メソッドって定義したっけ？全体検索したい　→「error_404」を全体検索

```
# @トップディレクトリ
$ grep -r error_404 .
```

