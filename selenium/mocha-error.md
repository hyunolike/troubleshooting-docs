## 문제
- `ERR_MOCHA_MULTIPLE_DONE` 발생 ㅠ,ㅠ

## 해결
- `afterEach` 구문에 `async-await` 추가
- selenium의 `Until.elementLocated(,)` `Until.elementIsVisible()` 추가


```javascript
...
afterEach(async function () {
    if (await this.currentTest.isFailed()) {
        await this.driver.takeScreenshot().then(
            await function (image) {
                filename = '2_error_screenshot.png'
                fs.writeFileSync(`report/screenshot/5_error_screenshot.png`, image, 'base64');
            }
        )
        await addContext(this, `../report/screenshot/5_error_screenshot.png`)
    }
})
...
it('2. placeholder text `이메일`으로 표기되는지', async function () {
    let by = By.id("ContentPlaceHolder1_txtId");
    await this.driver.wait(Until.elementLocated(by, 3000));
    let el = await this.driver.findElement(by);
    await this.driver.wait(Until.elementIsVisible(el), 3000);
    let 이메일_표기_확인 = await el.getAttribute('placeholder');

    assert.equal(이메일_표기_확인, "이메일");
})
```
