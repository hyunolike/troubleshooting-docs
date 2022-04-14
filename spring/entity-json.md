## 문제
- 연관관계 맵핑된 엔티티 JSON 변환 에러 발생 ㅠ.ㅠ
- 다른 연관관계 안맺은 엔티티는 정상적으로 변환 성공!
![image](https://user-images.githubusercontent.com/61215550/163336872-b96af7a7-355c-4835-a6db-29387b14ce5e.png)



## 해결
> [참고 자료](https://powernote.tistory.com/21)
- ✔ `DTO`는 마지막 리턴에서 변환해주면서 넘기자! 
- 양방향 관계? 로 인한 변환 에러
- `fetch = FetchType.LAZY` 문제
- 해결!! `@JsonBackReference` 어노테이션 추가

