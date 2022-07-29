## 문제
- 설정 마친 상태에서 서버 시작 후, 마이그레이션이 안되는 문제

## 해결
- ![image](https://user-images.githubusercontent.com/61215550/181703314-efbe0f48-57bc-4fc1-862d-565de602d42e.png)
- ✔ 폴더명 규칙 부분 잘못 된거였음
  - 기존: `V0_init.sql`
  - 해결: `V0__init.sql` >> `_` 이 부분 2번 연속 들어가야됨!
