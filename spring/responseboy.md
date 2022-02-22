## 문제
- `json` 배열을 넘기기 위해 객체 안에 리스트 객체 넣는 상황
-  하지만, 객체안에 리스트 객체가 안넣어지고 에러 발생

## 해결
- 자료구조 생각을 하지 못함

```java
@PostMapping
public CardListInfo.Data showCard(){
    List<CardList> list = new ArrayList<>(); 🤗
    for(int i=0; i<100; i++){
        list.add(CardList.builder().cardInfo("테스트"+ i).build());
    }
    CardListInfo.Data cardListInfo = CardListInfo.Data.builder().result(true).cardList(list).build(); 🤗
    return cardListInfo;
}
```

![image](https://user-images.githubusercontent.com/61215550/155083304-df0ecd1e-90c4-413d-92a2-aa5f4029030d.png)


## 추가
- 객체안에 객체안에 객체
    - `dto` 크게 3가지 필요 >> `Response` `CardListInfo` `CardList`

![image](https://user-images.githubusercontent.com/61215550/155087376-2651fea7-6680-4980-99ff-c0911bd52cb5.png)

```java
@PostMapping
public Response<CardListInfo.Data> showCard(){
    List<CardList> list = new ArrayList<>();
    for(int i=0; i<100; i++){
        list.add(CardList.builder().cardInfo("테스트"+ i).build());
    }
    CardListInfo.Data cardListInfo = CardListInfo.Data.builder().result(true).cardList(list).build();
    Response result = new Response<>(cardListInfo);

    return result;
}
```

![image](https://user-images.githubusercontent.com/61215550/155084390-36a15cea-60ea-475a-81e0-5b31d10d1843.png)
