## 문제
- 스프링에서 로그백 생성 로직 구현 후, 도커 내 컨테이너에서는 생성되지만 로컬쪽에서는 확인할 수 없는 문제

## 해결
- 도커 파일에 추가적으로 __바인드 마운팅__ 설정을 통해 해결해준다.

```yml
volumes:
  - D:\home\log:/home/log ✔
```
- ![image](https://user-images.githubusercontent.com/61215550/168502786-e0e373f5-cc1e-414b-991b-5968357a1524.png)
- ![image](https://user-images.githubusercontent.com/61215550/168502799-275ee3b1-5ad0-4e2f-b73c-00d10c24c189.png)
