## 문제
- 로컬 내 신규 도커 컴포즈이용한 디비로 띄운 상황
- 특정 테이블 insert 시 `primary` 키 중복 문제 발생

## 해결
> [참고자료](https://til.songyunseop.com/mysql/some_case_insert_with_duplicated_key.html)
- 3가지 방법
  1. `INSERT IGNORE`: 중복 발생시 지금 삽입 ROW 무시
  2. `REPLACE INTO`: 기존 ROW 삭제 > 지금 실행 ROW 삽입
  3. `ON DUPLICATE KEY UPDATE`: DUPLICATE KEY 일때 UPDATE 하는 쿼리

- ⭐일단 임의로 계속 `primary key` 증가시켜 중복안되게해서 insert 함!
  - 여기서 `primary key`는 자동증가 키!
- 다음에는 위 3가지 방법 중 하나 선택해 실행
