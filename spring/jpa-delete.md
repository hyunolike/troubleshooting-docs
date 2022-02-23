## 문제
- jpa 쿼리 메서드 생성 후, 서비스단 동작 안되는 문제!

`repository`
```java
void deleteByCardInfo(String cardInfo);
```


## 해결
- JPA에서는 객체 유지, 삭제하기 위해서 __트랜잭션__ 필요!
  - 파생된 삭제 쿼리 사용 시 `@Transactional` 주석을 사용해 트랜잭션 실행 유무 확인

`service`
```java
@Override
@Transactional
public void deleteCard(CardInfo.Request req) {
    cardRepository.deleteByCardInfo(req.getCardInfo());
}
```
