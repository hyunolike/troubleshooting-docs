## 문제
> [참고 자료](https://jjunii486.tistory.com/172)
- `java.lang.IllegalStateException: Unable to find a @SpringBootConfiguration, you need to use @ContextConfiguration or @SpringBootTest(classes=...) with your test`
- 기존 프로젝트에 테스트 패키지 자체가 없어서 메인 소스코드 패키지대로 만들지 않고 그대로 만들어서 진행하면 발생했던 문제

## 해결
- `@SpringBootApplication` 붙은 클래스가 존재하는 패키지의 하위 패키지에 테스트를 두면 해결이 된다.
