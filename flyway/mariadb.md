## 문제
> [참고자료](https://stackoverflow.com/questions/70923478/flywayexception-unsupported-database-mariadb-10-5)
- Maria DB 10.5 버전 지원 안하는 문제 

## 해결
- flyway 지원하는 버전으로 다운그레드!!! ✔


```
dependencies {
    description("Flyway")
    implementation group: 'org.flywaydb', name: 'flyway-core', version: '7.7.3'
}
```
