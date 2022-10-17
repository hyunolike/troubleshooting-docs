## 문제 
- could not install Gradle distribution from

## 해결 
- 환경 상태: 환경변수 gradle 버전 설정됨(스프링에 설정된 그레들 버전과 맞지 않은 듯) ✔
  - ![image](https://user-images.githubusercontent.com/61215550/182982271-86c8a664-d425-404e-aaea-a527084d897a.png)
- `gradlew --version` 터미널 실행 하게 되면 `gradle-wrapper.properties` 에 설정된 버전으로 다운로드 진행하게 됨
  - ![image](https://user-images.githubusercontent.com/61215550/182982316-6dd4f79f-c122-4fb9-a1cb-ae10d6bf36c3.png)
- 정상 작동 !! 

## 해결 `2022.10.17` 
- ⭐ 인텔리제이 그레들 설정 > `Specified location` 으로 직접 그레들 폴더 접근하도록 설정
- ![image](https://user-images.githubusercontent.com/61215550/196068441-cee2afb9-66e9-4cec-851e-ef07172e1472.png)

