## 문제
- jpql 업데이트 작성시 `Not supported for DML operations [UPDATE....`

## 해결
- 레포지토리 단 `@Modifying` 추가
- 서비스 단 `@Transactional` 추가


```java
@Modifying
@Query(value = "UPDATE 테이블 u " +
        "SET u.status = :STATUS " +
        "WHERE u.orderNo = :ORDER_NUM ")
void updateStatusFromOrder(@Param("ORDER_NUM") String orderNum, @Param("STATUS") String status);
```
