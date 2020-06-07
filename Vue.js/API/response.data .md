## axiosで使うresponse.dataって何？

axiosを使ってメソッド定義
```
list: function() {
        axios.get(`/lists.json`)
        .then(response => (
          this.list = response.data
           )
        );
      }
```

response.dataとは何？？


## レスポンスのうちの「データ」

> レスポンスには以下のようなものが入ります。
> 基本的にはresponse.dataにデータが返ることにだけ注意しておけば大丈夫です。
>
> ```
> // レスポンスデータ
> response.data
> // ステータスコード
> response.status
> // ステータステキスト
> response.statusText
> // レスポンスヘッダ
> response.headers
> // コンフィグ
> response.config
> ```
https://www.willstyle.co.jp/blog/2751/
