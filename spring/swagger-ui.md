## 문제
- 실행 과정 중 `'Failed to start bean 'documentationPluginsBootstrapper'; nested exception is java.lang.NullPointerException'` 에러 발생

## 해결
- 의존성 관련된 라이브러리 버전을 서로 맞춰주자 
  - 스프링 버전까지

```groovy
    id 'org.springframework.boot' version '2.5.2'

    implementation group: 'io.springfox', name: 'springfox-swagger2', version: '2.9.2'
    implementation group: 'io.springfox', name: 'springfox-swagger-ui', version: '2.9.2'
    implementation group: 'org.modelmapper', name: 'modelmapper', version: '2.3.8'
```
