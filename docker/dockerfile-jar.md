## 문제
```Dokcerfile
FROM amazoncorretto:17

# JAR_FILE 변수
ARG JAR_FILE=./build/libs/*.jar  ⭐️ 왼쪽 경로 위치를 찾지 못하는 문제 ㅠ,ㅠ 그래서 카피 에러가 지속적으로 나게 됨

# COPY 경로는 context 경로 안에 있어야 됨(중요)
COPY ${JAR_FILE} app.jar

ENTRYPOINT ["java", "-jar", "/app.jar" ,"--spring.profiles.active=local"]
```

## 해결
> [참고자료](https://bgpark.tistory.com/132)
- <img width="774" alt="image" src="https://user-images.githubusercontent.com/61215550/198830979-4c14d944-5d2c-4801-ae37-df113974417b.png">
