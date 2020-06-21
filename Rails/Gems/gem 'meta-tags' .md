## gem 'mata-tags' - metaタグをかく-

```display_meta_tags```メソッドを使ってmetaタグを記述できる
```
<%= display_meta_tags() %>
```

> ```
> <%= display_meta_tags({
>         :title => "" ,
>         :site => t('site') ,
>         :description => 'welcome todescpriton',
>         :keywords => 'ミニ四駆ギャラリー, ギャラリー, ミニ四駆, mini4wd',
>         :open_graph => {
>            :title => 'mini4wg -ミニ四駆ギャラリー',
>            :url   => root_url ,
>         },
>        :twitter => {
>             :card => 'product',
>             :site => '@mini4wg'
>         } ,
>        :viewport => "width=device-width, initial-scale=1.0" ,
>        :reverse => true
>     })
>   %>
> ```
https://qiita.com/yamitake@github/items/983b53ae96ef5364567b

### gem 'meta-tags' README

https://github.com/kpumuk/meta-tags
