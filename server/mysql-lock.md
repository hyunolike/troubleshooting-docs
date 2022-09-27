## 문제
```
DB에러는 아래 로그에서 registerMember 2번 연속으로 하면서

15:33:49.309 [http-nio-12345-exec-2] INFO  [c.m.b.common.aspect.ControllerAspect:29] : [started] registerMember
15:34:43.844 [http-nio-12345-exec-8] INFO  [c.m.b.common.aspect.ControllerAspect:29] : [started] registerMember
15:35:33.860 [http-nio-12345-exec-8] WARN  [o.m.jdbc.message.server.ErrorPacket:100] : Error: 1205-HY000: Lock wait timeout exceeded; try restarting transaction
15:35:33.863 [http-nio-12345-exec-8] WARN  [o.h.e.jdbc.spi.SqlExceptionHelper:137] : SQL Error: 1205, SQLState: HY000
15:35:33.864 [http-nio-12345-exec-8] ERROR [o.h.e.jdbc.spi.SqlExceptionHelper:142] : (conn=484) Lock wait timeout exceeded; try restarting transaction
15:35:33.872 [http-nio-12345-exec-8] ERROR [c.m.b.common.aspect.ControllerAspect:33] : [failed] registerMember
15:35:33.874 [http-nio-12345-exec-8] ERROR [c.m.b.common.aspect.ControllerAspect:34] : exception stack trace:
```

## 해결
- [참고자료](https://brunch.co.kr/@purpledev/4)
- 보통 100번 돌면 1번 정도 발생한다고 함 ㅠ,ㅠ
- 트랜잭션 수행 시간이 김 ~~~~~~
- 해결 방법 3가지
  1. `innodb lock wait timeout` 값 작게 설정 - `SELECT GLOBAL innodb_lock_wait_timeout = 20`
  2.  `Isolation level` 관련 
- 결론 >> 사전 모니터링 작업 필수!!!

### 2. Isolation level
- READ COMMITTED >> ⭐읽기 SELECT / 쓰기 트랜잭션 단위로 `lock` 걸림 ㅠ,ㅠ
  - commit된 데이터만 읽는 것을 허용하는 레벨
  - ✔`읽기 경우` SELECT 문장이 수행되는 동안 해당 데이터 >> `Shared lock` >> SELECT 완료 후 >> LOCK 해제!
  - ✔`쓰기 경우` 데이터 변경하는 동안 다른 트랜잭션 >> 해당 데이터 변경 불가!! wait 
- REPEATABLE READ - ⭐ MySQL의 Default level
  - 트랜잭션 첫 SELECT >> 해당 데이터에 Shared lock 걸고 데이터의 Snapshot 생성
  - 이후 동일 트랜잭션 내의 SELECT >> snapshot 읽게됨 


```java
@Transactional(isolation = Isolation.READ_COMMITTED)
```
