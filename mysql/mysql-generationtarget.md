## 문제
- JPA 테이블 생성 시 `GenerationTarget encountered exception accepting command : Error executing DDL via JDBC Statement`

## 해결
- JPA 설정 시 mysql 방언이 해당 프로젝트에 적합한지 확인
- 기존 `org.hibernate.dialect.MySQLInnoDBDialect` > 이걸로 `org.hibernate.dialect.MySQL5Dialect` 수정 후 정상 작동
