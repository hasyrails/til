## Untracked files 状態のファイルを消去する

```
$ git clean -(option)
```

https://it-ojisan.tokyo/git-untracked-clean/

### git clean で消去する対象のファイルを確認する

#### 方法１
```
$ git clean -i
```

#### 方法２

> ```
> $ git clean -dfn
> ```
> コマンドオプションの解説
> ・-nは確認をする
> ・-dはディレクトリも含める
> ・-fは強制的に行う
https://awesome-linus.com/2019/05/13/git-clean-untracked-files-delete/
