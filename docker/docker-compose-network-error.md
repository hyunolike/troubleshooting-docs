## 문제
- 기존 도커 컴포즈 이용한 프로젝트 새로 풀해서 실행 시, 네트워크 에러 발생하는 문제 ㅠ,ㅠ
  - `rror in docker: network "path" declared as external, but could not be found`
## 해결
- 도커 네트워크 생성하자
  - `docker network create "name_of_network"`
