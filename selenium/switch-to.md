## 문제
- 기존 `this.driver.switchTo().frame(0)` 방식으로는 해당 모달? 결제창 값 검증이 되지 않음 ㅠ,ㅠ

## 해결
> [참고자료](https://www.selenium.dev/selenium/docs/api/javascript/module/selenium-webdriver/lib/webdriver_exports_TargetLocator.html)
- ⭐`this.window()` 이용해서 값 검증을 진행!


```javascript
await this.driver.switchTo().window("sa_popup");
```


#### 1. 새로 열린 이니시스 창 내 `window.name` 입력(개발자 도구 이용)
#### 2. 해당 이름값을 위의 코드처럼 넣어서 창 변경 진행! 
