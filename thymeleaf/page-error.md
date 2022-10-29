## 문제
- `Exception processing template "/main": Error resolving template [/main], template might not exist or might not be accessible by any of the configured Template Resolvers`
- 로컬에선 잘 돌아갔지만 배포 이후???(도커) 에서 발생하는 문제

## 해결
> [참고자료](https://jg-han.tistory.com/100)
- <img width="831" alt="image" src="https://user-images.githubusercontent.com/61215550/198830166-2671562d-fb01-4c17-b4ee-c958d0fe57ec.png">
- 위에처럼 경로가 `//` 이렇게 인식되서 발생하는 문제였음 


```java
return 'main'; 
```
