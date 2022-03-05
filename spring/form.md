## 문제
```javascript
$(".modifyBtn").click(function (){
    if(!confirm("수정할꺼지????힛")){
        return ;
    }
    actionForm
    .attr("action", "/guestbook/modify")
    .attr("method", "post")
    .submit();
});
```
- 폼 요청 시 `org.springframework.validation.BindException` 에러 발생 

## 해결
- input 태그에 name 값도 같이 보내서 생기는 에러 ...ㅎ name 속성 제거 후 정상 작동
```javascript
<div class="form-group">
    <label>RegDate</label> ⭐ input 태그에 name 값도 같이 보내서 생기는 에러 ...ㅎ name 속성 제거 후 정상 작동
    <input type="text" class="form-control"  th:value="${#temporals.format(dto.regDate, 'yyyy/MM/dd HH:mm:ss')}" readonly>
</div>
<div class="form-group">
    <label>ModDate</label>
    <input type="text" class="form-control" th:value="${#temporals.format(dto.modDate, 'yyyy/MM/dd HH:mm:ss')}" readonly>
</div>
```
