## 문제
- 배포 후 배열 타입 인식 못해 내장함수 사용 불가하는 문제
  - 로컬에서는 동작
- ![image](https://github.com/hyunolike/troubleshooting-docs/assets/61215550/c6e8cd4a-2000-4aad-bcb8-9b7ca63a3116)

## 해결
> [참고자료](https://ko.javascript.info/nullish-coalescing-operator)
- nullish 추가


```js
array ?? []
```
