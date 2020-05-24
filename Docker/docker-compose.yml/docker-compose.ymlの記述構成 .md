## docker-compose.yml とは

・複数のコンテナを同時に動かす命令指令を設定する。  
・.yml形式のファイルなので、インシデントのネストが重要

## docker-compose.yml の記述構成

```
version:
services:
  [component1]:
    build:
      context:
      dockerfile:
    environment:
      [EnvironmentVariable1]:
      [EnvironmentVariable2]:
      ：
    command:
    tty:
    stdin_open:
    depends_on:
    ports:
    volumes:
    ：
  [component2]:
  　：
```
#### service: 直下のネストの要素名は任意で良い
上記のコードで```[component1]```,```[component2]```で示した箇所  
（services:の直下のネスト）は任意で自分で決めて良い。

#### 他の記述要素に関して

公式ドキュメントをみると他にも記述要素があるので、　　
どのネストに位置するかを情報確認しながら適宜理解する。

 
