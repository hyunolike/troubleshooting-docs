## 문제
- 유닛 테스트를 통해 데이터 삽입 테스트를 진행했느데 실제 MySQL에서 데이터가 제대로 넣어지지 않는 문제 발생

![image](https://user-images.githubusercontent.com/61215550/154872087-c49d88cd-5bd0-4bec-bad7-61530d358e1c.png)

## 해결
- 코드 잘못 파악함 ㅠ,ㅠ

```java
@Test
public void 직접_데이터_넣기() {
    Member member = new Member;
    member.builder() 🤷‍♂️ 이상한 코드 작성!! member = memeber.builder()... 이게 정답
            .name("장현호")
            .password("1111")
            .address("서울시 마포구")
            .build();
    memberRepository.save(member);
}
```


```java
  @Test
  public void 직접_데이터_넣기() {
      Member member = Member.builder()
              .name("장현호")
              .password("1111")
              .address("서울시 마포구")
              .build();
      memberRepository.save(member);
  }
```

![image](https://user-images.githubusercontent.com/61215550/154872205-a95f6686-f16a-4692-97d1-409774f86134.png)
