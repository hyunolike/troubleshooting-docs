## 문제
- 포스트맨으로 요청 시 `cannot deserialize from object value` 에러 발생

## 해결
- 기본 생성자가 없기 때문에 데이터 생성해서 반환하지 못하는 걸로 파악

```java
public class CardInfo {

    @Getter @Setter
    @Builder
    @ToString
    @AllArgsConstructor ✔
    @NoArgsConstructor ✔
    public static class Request{
        String cardInfo;
    }

    @Getter @Setter
    @AllArgsConstructor
    public static class Data{
        boolean result;
    }
}

```
