# 概要

Stateを持たないコンポーネント。関数型コンポーネントともいう。

## 宣言

[参考](https://medium.com/missive-app/45-faster-react-functional-components-now-3509a668e69f)

```javascript
import React, { FC } from 'react';

const App: FC = () => {
  return (
    <div className="App">
      {FunctionalComponent({title: "HELLO FC"})}
    </div>
  );
}

interface Props {
  title: string
}

const FunctionalComponent: FC<Props> = (props) => {
  return (
    <div>
      {props.title}
    </div>
  );
}
```

## 備考

- [クラスコンポーネントより45%早いらしい](https://medium.com/missive-app/45-faster-react-functional-components-now-3509a668e69f)
