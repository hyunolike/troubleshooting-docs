## 문제
- `channel.cd(remote)` 부분에서 경로 에러가 계속 발생 >> 여기서 권한 에러 ㅠ,ㅠ

## 해결
- ssh 서버 프로그램인 `freeFTPd` 유저 생성시 루트 경로를 `D:\` 로 설정해줘야 한다!
  - ✔ 유저 경로 설정 오류로 인한것
