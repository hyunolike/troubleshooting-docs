## 문제
- `@Builder` `@NoArgsConstructor` 함께 사용 시 에러 발생

## 해결
- 모든 멤버변수를 받는 생성자가 없는 것이 이유
- `@AllArgsConstructor` 추가

### Q. 왜 전체 멤버변수를 갖는 생성자가 필요한걸까?
일단, 의미 상 빌더 패턴을 생각해 보았을 때, 아무것도 없는 생성자는 필요가 없다.

빌더는 필드의 초기화 작업을 도와주는 역할이기 때문에.

Lombok 공식사이트 - @Builder 설명 中
Finally, applying @Builder to a class is as if you added @AllArgsConstructor(access = AccessLevel.PACKAGE) to the class and applied the @Builder annotation to this all-args-constructor. This only works if you haven't written any explicit constructors yourself.

또한, 위 내용으로 보았을 때
@Builder 사용 시, 생성한 생성자가 없다면 @AllArgsConstructor(access = AccessLevel.PACKAGE) 가 암묵적으로 적용된다고 한다. 반대로 생성한 생성자가 있다면 @AllArgsConstructor 적용이 반드시 필요한게 아닐까?.. (이건 추측)
