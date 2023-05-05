## 문제
- `docker ps` 명령어 안먹히는 문제
- <img width="837" alt="image" src="https://user-images.githubusercontent.com/61215550/236435520-243be602-566d-40b1-b89d-49eeea693055.png">

## 해결
- 런타임 오픈소스 사용 중 `colima` 
- `docker context ls` >> `docker context use desktop-linux` 명령어 실행 
  - desktop-linux 기본 도커 설치시 기본 런타임 소프트웨어
- <img width="578" alt="image" src="https://user-images.githubusercontent.com/61215550/236435765-f38b7b94-ec12-4a3e-b038-334abaa19850.png">
  
