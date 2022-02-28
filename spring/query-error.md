## 문제
> [참고 링크](https://hayeon17kim.github.io/posts/hiwork-07/)
- `org.springframework.dao.InvalidDataAccessResourceUsageException: could not extract ResultSet; SQL [n/a]; nested exception is org.hibernate.exception.SQLGrammarException: could not extract ResultSet`
- 스프링부트 테스트 진행 시 위와 같은 에러가 나옴

## 해결
- 디비 테이블명과 다르다는 사실을 뒤늦게 파악

```java
@Repository
public interface SchoolRepository extends JpaRepository<School, Long> {
    @Query(value = "select distinct(city) from sp_school ✔ " , nativeQuery = true)  ✔ (기존) school >> (수정) sp_school
    List<String> getCities();
}
```
