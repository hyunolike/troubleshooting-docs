## 문제
> [참고 링크](https://charliezip.tistory.com/21)

- `Failed to replace DataSource with an embedded database for tests. `
- `@DataJpaTest` 기본적으로 __ 내장된 메모리 데이터베이스(h2)__ 이용해 테스트 실행해주는데 여기서 마리아 디비라는물리적 데이터베이스에 연결해서 문제 발생

## 해결
- `AutoConfigureTestDatabase(replace = AutoConfigureTestDatabase.Replace.NONE)`

```java
@DataJpaTest
@AutoConfigureTestDatabase(replace = AutoConfigureTestDatabase.Replace.NONE)
class SchoolServiceTest {

    @Autowired
    private SchoolRepository schoolRepository;

    private SchoolService schoolService; // @Autowired 안됨 ??

    @BeforeEach
    void before(){
        this.schoolService = new SchoolService(schoolRepository);
    }


    @Test
    void 학교_생성(){
        School school = School.builder()
                .name("테스트 학교")
                .city("서울 강남구")
                .build();
        schoolService.save(school);

        // 입력 확인 테스트

        List<School> all = schoolRepository.findAll();
        assertEquals(1, all.size());
        assertEquals("테스트 학교", all.get(0).getName());
        assertEquals("서울 강남구", all.get(0).getCity());
    }
}
```
