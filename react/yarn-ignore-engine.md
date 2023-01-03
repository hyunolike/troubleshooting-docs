## 문제
- `node` 버전과 일치하지 않아 실행 거부하는 에러

## 해결
> [참고자료](https://velog.io/@2yunseong/The-engine-node-is-incompatible-with-this-module.-Expected-version-%EC%98%A4%EB%A5%98-%ED%95%B4%EA%B2%B0)
1. `yarn config list`
  - ![image](https://user-images.githubusercontent.com/61215550/210303950-9f2d27ce-deff-427b-8ccf-9844dac660a6.png)
2. `yarn config set ignore-engines true` 
  - ![image](https://user-images.githubusercontent.com/61215550/210304009-b9bd3c7f-c579-48c5-86eb-76a8be084d42.png)
