## 문제
- `async` 함수 내 서비스 로직단이 계쏙 `비동기` 처리되는 문제

## 해결
> [참고자료](https://tech-monster.tistory.com/180)
- ⭐ `Promise` 객체 반환 > 비동기 처리되는 함수!!! 라는 말
- `await` 함수를 사용하자 > 동기 처리되게끔 해준다!!


```js
const fun1 = async () => {
  await fn2 // 서버 통신 (Promise) 반환

  fn3 // 비동기 처리
  await fn4 // 동기 처리
}
```
