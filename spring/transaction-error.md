## 문제
```java
@Test
void 지역목록_가져오기(){
    List<String> list = schoolService.cities();
    assertEquals(1, list.size());
    assertEquals("서울 강남구", list.get(0));
}
```
- 테스트 코드 해당 부분에서 `Transaction silently rolled back because it has been marked as rollback-only` 에러 발생!

## 해결
```java
@Transactional ✔
@Rollback(value = false) ✔
@DataJpaTest
@AutoConfigureTestDatabase(replace = AutoConfigureTestDatabase.Replace.NONE)
class SchoolServiceTest {...}
```
- 테스트 클래스 어노테이션 부분 `@Transactional` 선언
  - 해당 테스트 커밋되는  순간 `rollback-only` 로 인한 에러로 파악
  - 가장 상단의 `@Transcational` 삭제 후 진행하면 해결 완료 :)
