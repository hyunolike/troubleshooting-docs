## 문제
- 아래와 같이 npm 설치시 경로 설정 잘못해서 발생 ㅠ,ㅠ


```
📦 루트 프로젝트
├─ ⭐️ node_module - 여기에 라이브러리 설치해서 에러 발생 ㅠ,ㅠ
├─ package.json
└─ package-lock.json
   └─ 자식 프로젝트 (개발 중)
      ├─ ⭐️ node_module 
      ├─ package.json
      └─ package-lock.json


One of your dependencies, babel-preset-react-app, is importing the
"@babel/plugin-proposal-private-property-in-object" package without
declaring it in its dependencies. This is currently working because
"@babel/plugin-proposal-private-property-in-object" is already in your
node_modules folder for unrelated reasons, but it may break at any time.
```

## 해결
- 프로젝트 경로에 npm install 다시 실행!
