## 문제 
- `org.hibernate.tool.schema.spi.CommandAcceptanceException: Error executing DDL`
- `user` 테이블 명 생성 시 발생되는 에러

## 해결
- DB 메타데이터에 `USER` 테이블이 이미 존재하는 경우
- 테이블 명 `USRE` >> `TB_USER` 로 변경 ✔
