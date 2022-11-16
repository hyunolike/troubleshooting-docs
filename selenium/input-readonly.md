## 문제
> [참고자료](https://www.quora.com/How-do-I-get-text-for-a-read-only-input-field-box-using-Selenium-WebDriver)
- `input` - readOnly 속성인 값 못가져오는 문제
- ![image](https://user-images.githubusercontent.com/61215550/202054264-2f7ec526-bf91-42f3-ab00-76c35b15606e.png)

## 해결
- `.getAttribute('value')` 값 사용⭐


```java
String str = driver.findElement(By.name('TextBox1')).getAttribute('value');
```
