## propsプロパティ -データを親コンポーネントから子コンポーネントへ-

### 親コンポーネント
```data```オプションで
子コンポーネントに渡すデータを指定

> 【ComponentParent.vue】
> ```
> <template>
>  <div class="parent">
>   <component-children v-bind:variable="message" />
>  </div>
> </template>
> 
> <script>
>  import ComponentChildren from './ComponentChildren.vue'
>  export default {
>   name: 'ComponentParent',
>   components: {
>    ComponentChildren
>   },
>   data: function() {
>    return {
>     message: 'Hello Vue !!'
>    }
>   }
>  }
> </script>
> ```

### 子コンポーネント
```props```オプションで
親コンポーネントから受け取るデータを指定する

> 【ComponentChildren.vue】
> ```
> <template>
>  <div class="child">
>   <p class="received">{{ variable }}</p>
>  </div>
> </template>
> 
> <script>
>  export default {
>   name: 'ComponentChildren',
>   props: [
>    'variable'
>   ]
>  }
> </script>
> ```

https://designsupply-web.com/knowledgeside/4778/
