## 문제
> [참고 링크](https://jamong-icetea.tistory.com/173)
- 테스트 코드 실행 시 
  - `Validation failed for query for method public abstract ... ` 
- jpa 쿼리 출력 오류

## 해결
- `@Query` 어노테이션으로 네이티브 쿼리 수행하기 위해선 ✔ `nativeQuery` 속성 __true__

```java
@Repository
public interface SchoolRepository extends JpaRepository<School, Long> {
    @Query(value = "select distinct(city) from school" , nativeQuery = true) ✔
    List<String> getCities();
}
```

