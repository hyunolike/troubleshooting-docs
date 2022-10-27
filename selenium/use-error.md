## 문제
- ![화면 캡처 2022-10-27 123846](https://user-images.githubusercontent.com/61215550/198185935-afa9b8c9-b2a5-4c0a-a5d0-afcf30b78e4a.png)

## 해결
> [참고자료](https://stackoverflow.com/questions/67349350/experimental-chrome-options-in-selenium-node-js)
- 에러 코드를 내뱉지만 실제 동작에는 문제가 없음
- 따라서 에러 로그 안보이는 방향으로 다들 해결함 - 스택오버플로우


```javascript
const {Builder} = require('selenium-webdriver')
const chrome = require('selenium-webdriver/chrome'); 

const chromeOptions = new chrome.Options()
chromeOptions.excludeSwitches("enable-logging")

let driver = await new Builder().forBrowser('chrome').setChromeOptions(chromeOptions).build();
```
