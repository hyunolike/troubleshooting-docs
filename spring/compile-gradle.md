## 문제
- 코드상 `compile()` 부분에서 에러 발생

## 해결
> [참고자료](https://velog.io/@g0709-19/Gradle-Could-not-find-method-compile-%ED%95%B4%EA%B2%B0-%EB%B0%A9%EB%B2%95
- `Gradle 4.10` 이후 deprecate !!
- `complie()` >> `implementation()` 으로 수정
