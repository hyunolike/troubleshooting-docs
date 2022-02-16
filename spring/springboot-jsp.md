## 문제
- 기존 스프링부트를 이용해 `jsp` 서버 템플릿 엔진으로 프로젝트를 구성
- 하지만, 파일 구조 및 연결이 지속적으로 안되는 문제점

## 해결
> [참고 링크](https://7942yongdae.tistory.com/115)
- 별도의 라이브러리 및 jsp에 맞는 파일 구조 새로 구성
  - 자동으로 구성된 파일 구조는 `Thymeleaf` 엔진을 바로 사용 할 수 있다.
- 라이브러리: `tomcat-embed-jasper` 
- 파일 구조
![image](https://user-images.githubusercontent.com/61215550/154215375-c61117d8-a856-45fe-b9fc-c6edeeab9099.png)


- 그 다음으로는 `뷰 리졸버` 설정 변경해야 된다.
```yml
spring:
  mvc:
    view:
      prefix: /WEB-INF/view/
      suffix: .jsp
```

- 결과적으로 controller를 실행하게 되면
```java
@Controller
public class TempController {
    @GetMapping("/temp/home")
    public String tempHome() {
        System.out.println("tempHome()");
        return "home";
    }
}
```
- 간혹 
![image](https://user-images.githubusercontent.com/61215550/154215790-ed956878-929f-404b-8b6d-98ce8bdebbb1.png)
- 해당 라이브러리가 제대로 설정되어 있지 않기 때문에 발생이 되는거다.
