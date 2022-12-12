## 문제
- vue 3.0 설치시 발생하는 에러 
  - 여기서 뷰는 vue-cli
- `npm ERR! code EEXIST, file already exists, cmd shim`
  
## 해결
- 제거하자
  - `vue uninstall -g vue-cli`
- Vue 버전 2 `npm install -g vue-cli`
- Vue 버전 3 `npm install -g @vue/cli`
