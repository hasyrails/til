### マージ済のブランチをまとめて削除

``` 
$ git branch --merged|egrep -v '\*|develop|master'|xargs git branch -d
```

#### ```git branch -d```でも削除できるが‥
```
$ git branch 'branch-name' -d
```
でも削除はできるが１つ１つ削除しなければならず面倒

### 参考

[Gitでマージ済みブランチを一括削除 - Qiita](https://qiita.com/hajimeni/items/73d2155fc59e152630c4)
