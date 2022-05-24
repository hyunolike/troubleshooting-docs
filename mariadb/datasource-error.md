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

## 추가
### 스프링에서 데이터베이스 접속을 하지 못하는 경우 해결책
1. `application.yml` 파일에 데이터 소스 추가
2. `Configuration` 생성(Bean 이용한 디비 사용)
```java
@Configuration
public class DBConfiguration {
    @Bean
    public DataSource datasource() {
      return DataSourceBuilder.create()
      .driverClassName("")
      .url("")
      .username("")
      .password("")
      .build(); 
    }
}
```
3. `DataSourceAutoConfiguration` 제외(디비 사용안한다는 뜻)

```java
@SpringBootApplication(exclude={DataSourceAutoConfiguration.class})
public class Sample01Application {
	public static void main(String[] args) {
		SpringApplication.run(Sample01Application.class, args);
	}
}
```
