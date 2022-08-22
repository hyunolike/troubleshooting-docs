## 문제
- 스프링부트로 구현한 서버에서 json 객체 뿌리지 못함 ㅠ,ㅠ 

## 해결
- `Object` 타입으로 그대로 랜더링 불가 ✔


```javascript
<ul>
    {JSON.stringify(users)}
</ul>
```
- ![image](https://user-images.githubusercontent.com/61215550/185866503-05cce488-37b3-4e2d-a7ed-52b475beea67.png)
