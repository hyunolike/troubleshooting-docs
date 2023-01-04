## 문제
```sol
_ownedTokens[from].length--;
```


- ✅ 함수 에러 ㅠ,ㅠ


## 해결
- 버전 다운그레이드
- `pragma solidity >=0.4.24 <0.5.6;`
