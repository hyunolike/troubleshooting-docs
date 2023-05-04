## 문제
- `No serializer found for class` 에러 발생

## 해결
> [참고자료](https://stackoverflow.com/questions/59578802/jackson-no-serializer-found-for-class-and-no-properties-discovered-to-cre)
- `@Getter` 없어 사용자 정의 클래스 JSON 파싱 불가해서 발생하는 문제
- getter 함수 추가! 
