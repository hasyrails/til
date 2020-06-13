## not staged　状態のファイルを消去する。

not staged状態のファイルを取り消す
(git add前の変更を取り消す)

```
$ git checkout <FileName on 'not staged'>
```

not staged状態にあるファイルの変更を全て取り消したい場合
```
$ git checkout .
```


https://www.yoheim.net/blog.php?q=20140201

## git restore - ファイル変更を取り消す -

Gitバージョン2.23.0の新コマンドらしい  
https://qiita.com/yukibear/items/4f88a5c0e4b1801ee952

ファイルの変更を取り消す
```
git restore <filename>
```
