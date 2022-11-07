## 문제
- 셀레니움 테스트 시, `document` 객체 사용해 검증 시도
- 하지만, `ReferenceError: document is not defined` 에러 발생

## 해결
> [참고자료](https://bobbyhadz.com/blog/javascript-referenceerror-document-is-not-defined)
- node.js는 브라우저 환경을 제공하지 않고 서버 측 런타임이므로 `document` 객체 사용 불가 ㅠ,ㅠ 
- 해결 불가..ㅎ
