## docker run　を実行した時に走るターミナルコマンドを指定

例えばDockerfileの中身が次のようになっているとする
```
FROM <image>
：
：
CMD['git','status']
```

```$docker build　-t <ImageName>```でイメージ構築  
```$docker run <ImageName>```でコンテナ実行  
→CMDで指定されているコマンドである  
```
$ git status
```
が実行されることになる。

（Excelのマクロモジュールみたいなもの‥と考えたら怒られるだろうか）
