## 문제
- `useState` 바로 저장 후 사용할려 했지만 사용이 안되는 문제

## 해결
> [참고자료](https://velog.io/@hnsoo/useState-%EC%A0%95%EB%A6%AC)
- ⭐`setState()` 다음 렌더링에서 사용될 상태 변수를 업데이트한다!
  - 바로 state를 사용하게 되면 다음 렌더링이 실행되지 않았기에 변경전 state 값을 가지고 있게 된다.
- 새 state값과 이전 state 값이 같을 경우 리렌더링을 건너뛴다
- 모든 이벤트 핸들러 실행되고 나서 `setState()` 함수 호출해 화면 업데이트!


![image](https://github.com/hyunolike/troubleshooting-docs/assets/61215550/b06df1e7-e641-4be2-aae2-5274bdc8e756)
