## 문제
- `ElementClickInterceptedError: element click intercepted:`
- 해당 클릭 대상이 다른 요소로 가려져서 발생되는 문제
- 보통 에니메이션 포함된 페이지 로드될때 발생 >> 셀레늄 사이드 러너 사용 시 발생
## 해결
- 해당 페이지 내 스크롤, 화면 또는 로딩 시간 체크 후 딜레이 걸어줌
