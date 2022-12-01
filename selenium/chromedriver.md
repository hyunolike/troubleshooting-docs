## 문제
> [참고자료](https://codechacha.com/ko/selenium-chromedriver-version-error/)
- `SessionNotCreatedException: Message: session not created: This version of ChromeDriver only supports Chrome version 76`
- 드라이버 동작 안되는 문제

## 해결
- 크롬드라이버를 현재 크롬 브라우저 버전에 맞춰서 **버전 업** 을 진행!



```
 "chromedriver": "^107.0.3",
```
