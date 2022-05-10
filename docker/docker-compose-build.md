## 문제
```yml
version: "3.8"
services:
  spring-server:
    image: openjdk:8-jre
    ports:
      - "8888:8181"
    container_name: spring_server
    links:
      - mssql
    entrypoint: ["java", "-jar", "/app/spring-docker-0.0.1-SNAPSHOT.jar"]
```
- 위와 같이 작성 후 도커 컴포즈 빌드하게 되면 해당 서비스 실행되지 않는 문제

## 해결
- 볼륨으로 파일을 마운트 해준다!
- ![image](https://user-images.githubusercontent.com/61215550/167523007-74b683a6-cd44-4829-b555-f4bdd0fdbb62.png)


```yml
version: "3.8"
services:
  spring-server:
    image: openjdk:8-jre
    ports:
      - "8888:8181"
    container_name: spring_server
    links:
      - mssql
    volumes:
      - ../build/libs:/app ✔ [로컬 경로]:[도커 컨테이너 경로]
    entrypoint: ["java", "-jar", "/app/spring-docker-0.0.1-SNAPSHOT.jar"]
```
