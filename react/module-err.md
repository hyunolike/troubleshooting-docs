## 문제
- `Warning: Rendering <Context> directly is not supported and will be removed in a future major release. Did you mean to render <Context.Consumer> instead?`

## 해결
> [참고자료](https://stackoverflow.com/questions/71285222/rendering-context-directly-is-not-supported-and-will-be-removed-in-a-future-ma)
- 모듈 선언 시 `{ }` 추가


```js
import ColorProvider from './contexts/color';
import { ColorProvider } from './contexts/color';
```


### `{ } ` 차이
- `export` 방식 차이
  - ✔ `export` 내보낸 경우 >> `{}` 감싸 가져와야함
  - ✔ `export default` 내보낸 경우 >> 괄호 없이 가져올 수 있음
