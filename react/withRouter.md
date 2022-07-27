## 문제
- v6 버전에서는 해당 문법 사라짐 ㅠ,ㅠ

## 해결
- 문법 변경


```javascript
⭐⭐ 기존
dispatch(loginUser(body))
    .then(response => {
        if (response.payload.loginSuccess) {
            props.history.push('/') ✔
        } else {
            alert('Error˝')
        }
    })
⭐⭐ 변경
dispatch(loginUser(body))
    .then(response => {
        if (response.payload.loginSuccess) {
            navigate('/'); ✔
        } else {
            alert('Error˝')
        }
    })
```
