## 문제
- ![image](https://user-images.githubusercontent.com/61215550/208346789-5f0f75c9-3f29-4653-ae49-b024737c4773.png)
- `primary key` 중복? 유니크 하지 않다는 에러 발생ㅠ,ㅠ

## 해결
```js
data() { //변수 생성
  return {
    requestBody: this.$route.query + Math.floor(Math.random() * 101), ⭐ 랜덤값 추가로 해결!
    idx: this.$route.query.idx,
    title: '',
    author: '',
    contents: '',
    created_at: ''
  }
```


- ![image](https://user-images.githubusercontent.com/61215550/208358192-6057f31e-8af3-4a67-880a-79b59fbdec0d.png)
