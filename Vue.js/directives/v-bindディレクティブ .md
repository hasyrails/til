## v-bindディレクティブ -属性を動的に変更できるよう紐づける-

> Vueでアプリケーション作成をする際に  
> aタグのhref属性やimgタグのsrc属性なども動的に変更したい！  
> という場面があったりすると思います。そんな時に使えるのがVueのv-bindディレクティブです。  
>  
> 例えばボタンによってimgタグのsrc属性を切り替えて表示される画像を動的に切り替える  
> …などの場面で使用します。
> 
> v-bindディレクティブを用いれば動的に切り替えたい属性に切り替えるための変数を
> 紐づけしておくだけでこれらを実現してくれます。
https://www.e-loop.jp/knowledges/8

## v-bind ディレクティブの使い方

属性とのひもづけ
```
v-bind:<AttributeName>
```

```Vue.js
new Vue({
 el: "#app",
 data: { 
   ImageURL: "http://hogehoge/image",  // 変数ImageURLを定義
 },
 template: `
 <div>
   <img v-bind:src="ImageURL"/>　//src属性に変数ImageURLをひもづけ
 </div>
 `
})
```
