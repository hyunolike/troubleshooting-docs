## 문제
- 기존 ajax함수를 콜백 함수로 비동기 처리해서 넘기려고 했지만 `undefined` 나면서 에러나는 이슈

## 해결
- ajax 함수 내 성공 코드 에 다음 프로세스 콜백 함수를 넣어서 진행되도록 해결 함
- ![image](https://github.com/hyunolike/troubleshooting-docs/assets/61215550/a9db193e-61fc-4c6e-b5e6-54eac3963eb7)
