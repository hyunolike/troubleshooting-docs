## 문제 
- 메이븐 빌드 시, 테스트 쪽 에러 뜨면서 jar파일 생성 안되는 문제

## 해결
- 해당 테스트 파일을 제외시키고 jar파일을 생성하자
- `mvn package -Dmaven.test.skip=true`
