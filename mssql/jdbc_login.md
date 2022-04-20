## 문제
> [참고 자료 1](https://okky.kr/article/220386) <br>
> [참고 자료 2](https://docs.microsoft.com/ko-kr/sql/connect/jdbc/system-requirements-for-the-jdbc-driver?view=sql-server-ver15)
- `Spring Boot` 를 이용해 `MSSQL` 연동시 발생하는 문제
- 에러는 무슨 드라이버 설정? 에러 및 로그인 에러 2개 발생

## 해결
### 1. 해당 `yml` 파일 설정에서 윈도우 통합 인증 로그인 설정을 지워주자
- `integratedSecurity=true`
```yml
url: jdbc:sqlserver://localhost:1433;DatabaseName=udm;integratedSecurity=true;encrypt=true;trustServerCertificate=true ❌
url: jdbc:sqlserver://localhost:1433;DatabaseName=udm;encrypt=true;trustServerCertificate=true ⭕
```

### 2. 그 다음으로 공식 mssql에서 jdbc 라이브러리를 직접 다운로드 받아 외부 설정을 해준다.
![image](https://user-images.githubusercontent.com/61215550/164156192-446dd412-a38a-469c-b2b3-517b9160dc18.png)

```java
dependencies {
    description("mssql 연결을 위한 라이브러리")
    implementation files('libs/mssql-jdbc-10.2.0.jre8.jar')
}
```
- 자바 버전별 지원하는 jdbc가 다르다.
- ![image](https://user-images.githubusercontent.com/61215550/164156390-fcf46b3a-5c0a-4759-8315-657f75fbeb7d.png)
