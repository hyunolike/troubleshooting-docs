## 문제
- Could not convert socket to TLS

## 해결
> [참고자료](https://shanepark.tistory.com/426)
- 프로토콜 강제 설정
  - `TLSv1.2`
- java mail 버전 설정



```
// EMAIL
// https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-mail
implementation 'org.springframework.boot:spring-boot-starter-mail'

// https://mvnrepository.com/artifact/com.sun.mail/javax.mail
implementation 'com.sun.mail:javax.mail:1.6.2'
```
