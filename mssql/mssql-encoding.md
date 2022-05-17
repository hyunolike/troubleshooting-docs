## 문제
- 데이터 삽입 시 `???` 나오는 문제
- 추후 따로 정리 `encoding`

## 해결
```sql
select @@language; ✔ 언어 확인

SELECT collation_name ✔collation_name 확인
FROM sys.databases
WHERE name = '데이터베이스 명';

ALTER DATABASE 데이터베이스 명 SET SINGLE_USER WITH ROLLBACK IMMEDIATE; ✔ 싱글유저 모드로 변경 / 싱글유저로 접속하지 않으면 다른 사람의 작업으로 인해 배타적잠금 오류 발생
ALTER DATABASE 데이터베이스 명 COLLATE Korean_Wansung_CI_AS;
ALTER DATABASE 데이터베이스 명  SET MULTI_USER; ✔ 멀티유저 모드로 변경
```
- 정상적으로 삽입 확인 가능! ✔
