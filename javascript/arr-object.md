## 문제
- 배열 내 객체 속성 접근 안되는 문제


```js
const arr = [
  {
    key1: value1,
    key2: value2
  },
  ...
]

⭐ arr[arr.length].key1 // 속성 접근 안됨!!!!!
```
## 해결
- 옵셔널 체이닝 `'?.` 사용


```js
arr[arr.length]?.key1
```
