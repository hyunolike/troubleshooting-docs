## 문제 
- could not install Gradle distribution from

## 해결 
- 환경 상태: 환경변수 gradle 버전 설정됨(스프링에 설정된 그레들 버전과 맞지 않은 듯) ✔
- `gradlew --version` 터미널 실행 하게 되면 `gradle-wrapper.properties` 에 설정된 버전으로 다운로드 진행하게 됨
- 정상 작동 !! 
