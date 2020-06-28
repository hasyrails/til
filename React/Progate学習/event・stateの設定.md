## eventの設定
``` jsx
# == clickイベント発火時にボタン表記文字をコンソール出力させる ==
<button onClick={() => {console.log('ひつじ仙人')}}>ひつじ仙人</button>
```

## stateの設定
```jsx
import React from 'react';

class App extends React.Component {
// constructor/superはおまじない
  constructor(props) {
    super(props);
    // stateを定義
    this.state = {name: 'にんじゃわんこ'};
    
  }
  
  render() {
    return (
    	<div>
    	  <h1>こんにちは、にんじゃわんこさん！</h1>
        <button onClick={() => {console.log('ひつじ仙人')}}>ひつじ仙人</button>
        <button onClick={() => {console.log('にんじゃわんこ')}}>にんじゃわんこ</button>
      </div>
    );
  }
}

export default App;

```
