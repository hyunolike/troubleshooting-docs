## 문제
- h2 driver 못찾아옴

## 해결
- 테스트 시에만 작동되게 해놓은거였음 !!


```gradle
testCompile group: 'com.h2database', name: 'h2', version: '1.4.200' ❌ 변경전
implementation 'com.h2database:h2:1.4.200' ⭐⭕ 변경 후!!
```
