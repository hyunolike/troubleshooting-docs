## 문제 
- 스프링부트 이용한 프로젝트로 `yml` 파일에 해당 디비 접속 정보를 작성했지만 
- 인식하지 못하는 에러 발생

## 해결
- `datasource` >> `database` 로 작성해서 발생했던 문제(아주 사소한) 
```yml
spring:
  datasource: ✔
    url: jdbc:mariadb://localhost:3306/[스키마 명]
    driver-class-name: org.mariadb.jdbc.Driver
    username: root
    password: 1111
```
