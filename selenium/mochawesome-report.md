## 문제
- 설정으로 해당 양식에 맞게 출력되도록 구성했지만 결과는 ... 안나옴..ㅎ


```javascript
module.exports = {
    reporter: 'node_modules/mochawesome',
    'reporter-option': [
        'overwrite=true',
        'reportDir=test-report',
        'reportFileName=[status]_[datetime]-[name]-report', ⭐
        'showPassed=false',
        'timestamp=longDate',
        'code=false'
    ],
}
```

## 해결
- `reportFileName` -> `reportFilename` ✔ 대소문자 잘구별하자ㅋㅋㅋㅋㅋㅋㅋㅋ


```javascript
module.exports = {
    reporter: 'node_modules/mochawesome',
    'reporter-option': [
        'overwrite=true',
        'reportDir=test-report',
        'reportFilename=[status]_[datetime]-[name]-report', ⭐
        'showPassed=false',
        'timestamp=longDate',
        'code=false'
    ],
}
```
