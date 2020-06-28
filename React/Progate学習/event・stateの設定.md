## eventの設定
``` jsx
# == clickイベント発火時にボタン表記文字をコンソール出力させる ==
<button onClick={() => {console.log('ボタンを押してね')}}>ボタンを押してね</button>
```

## stateの設定/変更
```jsx
import React from 'react';

class App extends React.Component {
// constructor/superはおまじない
  constructor(props) {
    super(props);
    // stateを定義
    this.state = {name: 'ねこ'};
    
  }
  
  render() {
    return (
    	<div>
    	  <h1>こんにちは、にんじゃわんこさん！</h1>
        <button onClick={() => {this.setState({name: 'ひつじ'})}}>ひつじ</button>
        <button onClick={() => {this.setState({name: 'ねこ'})}}>ねこ</button>
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
    this.state = {name: 'ねこ'};　
  }
  
  // handleClickメソッドを定義
  handleClick(name){
    this.setState({name: name}); 
  }
  
  render() {
    return (
    	<div>
    	  <h1>こんにちは、{this.state.name}さん！</h1>  {/*  こんにちは、ねこさん！ */}
    	  {/* handleClickメソッドでstate変更する */}
        <button onClick={() => {this.handleClick('ひつじ')}}>ひつじ</button>
        <button onClick={() => {this.handleClick('ねこ')}}>ねこ</button>
        
      </div>
    );
  }
}

export default App;
```
