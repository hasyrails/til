## eventの設定
``` jsx
# == clickイベント発火時にボタン表記文字をコンソール出力させる ==
<button onClick={() => {console.log('ひつじ仙人')}}>ひつじ仙人</button>
```

## stateの設定/変更
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
        <button onClick={() => {this.setState({name: 'ひつじ仙人'})}}>ひつじ仙人</button>
        <button onClick={() => {this.setState({name: 'にんじゃわんこ'})}}>にんじゃわんこ</button>
      </div>
    );
  }
}

export default App;

```

### stateの値は直接代入で変えることはできない

```setState```メソッドで変更する。

## メソッドの定義
```jsx
import React from 'react';

class App extends React.Component {
  constructor(props) {
    super(props);
    this.state = {name: 'にんじゃわんこ'};
  }
  
  // handleClickメソッドを定義
  handleClick(name){
    this.setState({name: name});
  }
  
  render() {
    return (
    	<div>
    	  <h1>こんにちは、{this.state.name}さん！</h1>
    	  {/* handleClickメソッドでstate変更する */}
        <button onClick={() => {this.handleClick('ひつじ仙人')}}>ひつじ仙人</button>
        <button onClick={() => {this.handleClick('にんじゃわんこ')}}>にんじゃわんこ</button>
        
      </div>
    );
  }
}

export default App;
```
