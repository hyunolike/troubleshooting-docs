## 문제
```java
afterEach(async function () {
    if(this.currentTest.isFailed()){
        this.driver.takeScreenshot().then(
            function (image){
                filename = '#1_error_screenshot.png'
                fs.writeFileSync(`screenshot/#1_error_screenshot.png`, image, 'base64');
            }
        )
        addContext(this, `../screenshot/#1_error_screenshot.png`) ⭐ 
    }
})
```


- `http://localhost:63342/hhjang/screenshot/#1_error_screenshot.png` ⭐ 이미지 경로가 이렇게 잡힘 ㅠ,ㅠ

## 해결
- 그냥 기본 루트 파일쪽에 위치 시키자..
