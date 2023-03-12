## 문제
- 스프링 서버 실행 시, 데이터 쿼리 동작 안되는 문제

## 해결
> [참고자료](https://devvkkid.tistory.com/262)

### 1. 스프링 버전 및 `sql.init.mode` 이슈
```sql
// build.gradle.kts
plugins {
    id("org.springframework.boot") version "2.5.13"
 
// application.yml
spring:
  sql:
    init:
      mode: always

```
### 2. auto-commit: false
- 스프링부트 2.5.0 이하 버전 

### 3. defer-datasource-initialization
- 스프링부트 버전 관련
