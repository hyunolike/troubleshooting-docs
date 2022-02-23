## 문제
- 인터넷 상에 나온 `SecurityContextHolder의 Principal`를 통한 객체 얻어오는 방법은 필요하지 x (해당 객체는 자바 표준 Principal 객체)
  - 커스텀된 `User` 디비를 통해 값을 얻고 싶다. 

## 해결
- [참고링크](https://ncucu.me/137)
- `AuthenticationPrincipal` 애노테이션 사용해서 UserDetailService에서 return한 객체를 파라메터로 직접 받기!


```java
@PostMapping("/getCardList")
public Response<CardListInfo> showCardList(@AuthenticationPrincipal User user){
    List<CardList> cardLists = cardService.showCardList(user);

    CardListInfo.Data cardListInfo = CardListInfo.Data.builder().result(true).cardList(cardLists).build();
    Response result = new Response<>(cardListInfo);

    return result;
}
```
