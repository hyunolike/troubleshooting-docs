## 문제
- 스프링 부트 메인을 실행하면 서버가 다운되는 현상

## 해결
- `Gradle` 의존성 중 __tomcat__ 으로 인한 이슈
- 아래의 의존성 제거 후 실행
- [스택오버플로우 참고 링크](https://stackoverflow.com/questions/22380119/why-does-my-spring-boot-app-always-shutdown-immediately-after-starting)
- `providedRuntime`은 런타임 시점에 의존성 제공 > 여기서 이슈 발생! 

`providedRuntime 'org.springframework.boot:spring-boot-starter-tomcat'`

```
providerRuntime은 런타임 시점에 의존성을 제공해야하기 때문에 발생하는 문제로 보입니다.

톰캣을 사용하여 실행한 상태가 아니기 때문에 웹 모듈(환경)이 실행되지 않는 상태인 거죠.

providedRuntime을 제거하면 실행되는 이유는 기본 web 의존성에 complie '....tomcat' 포함되기 때문이구요.

PC에 설치되어있는 톰캣으로 실행하시는게 아니라면 그냥 제거하고 실행하시는게 맞습니다.
```

