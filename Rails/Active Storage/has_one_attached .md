## ```has_one_attached```

> Commentモデルに1つの画像を添付するには、has_one_attachedを使います。
>
> ```ruby
> class Comment < ApplicationRecord
>   has_one_attached :image
> end
> ```
> :imageはファイルの呼び名で、:photo、:avatar、:hogeなど、ファイルの用途に合わせて好きなものを指定してください。
> ここで、Imageモデルなどを作る必要はないです。
> Active Storageは裏側でBlobとAttachmentモデルを使って、こそこそとcomment.imageを使えるようにしてくれます。(有能すぎ)
https://qiita.com/hmmrjn/items/7cc5e5348755c517458a

### ```Blob```モデル/```Attachment```モデル 
```Blob```モデルと```Attachment```モデルは
```
$ rails active_storage:install
$ rails db:migrate
```
で作られるActiveRecordの持つモデル
