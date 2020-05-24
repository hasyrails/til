## イメージを構築する docker build

・PATH : Dockerfileがある場所のプロジェクト内のパス  
・URL : DockerfileがあるURL (Gitリポジトリなど)  
とする

PATHにあるDockerfileからイメージを構築するときは
```
docker build [OPTIONS] PATH
```

URLにあるDockerfileからイメージを構築するときは
```
docker build [OPTIONS] URL
```
## docker build　コマンドで使用できるオプション

・　-tオプション　：　ビルドするイメージに名前をつける




