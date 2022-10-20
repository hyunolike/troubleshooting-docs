## 문제
> [참고자료](https://ipex.tistory.com/entry/Selenium%EC%9B%B9%EC%9E%90%EB%8F%99%ED%99%94-async-Iterator-%EC%9C%A0%EC%9D%98%EC%82%AC%ED%95%AD-findElements-Bycss)
- selenium js 는 모든 동작이 비동기 방식!!
- A, B, C 의 findElement 가져오게 되면 `Promise<Pending> (Array)` 로 가져오게 됨 .. 이게 문제 .. 값을 못 갖고옴

## 해결
- `async` `await` 함수 사용!
