## 문제
> [참고자료](https://codechacha.com/ko/selenium-chromedriver-version-error/)
- `SessionNotCreatedException: Message: session not created: This version of ChromeDriver only supports Chrome version 76`
- 드라이버 동작 안되는 문제

## 해결
- 크롬드라이버를 현재 크롬 브라우저 버전에 맞춰서 **버전 업** 을 진행!



```
 "chromedriver": "^107.0.3",
```


|크롬 브라우저 버전|크롬 드라이버 버전|
|---|---|
|![image](https://user-images.githubusercontent.com/61215550/205182290-f37b81b7-d6f8-4315-b88a-848f41204648.png)|![image](https://user-images.githubusercontent.com/61215550/205182318-394a9bf7-bf8e-4b65-a604-c2c02edae371.png)|
