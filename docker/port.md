## 문제
- `Ports are not available, Container Name "/XXX" is already in use by container` 에러 명
- `PS C:\Users\hh.jang> docker run --name mariadb_kona -p 3308:3306 -e MYSQL_ROOT_PASSWORD=kona1234 -d 620b63fe3891`
- 위와 같이실행 후 외부 접속 포트로 연결이 안됨

## 해결
- 현재 `3306` `3307` 포트는 각각 mysql, mariadb 설정된 포트였기에 다른 포트로 설정 후 정상 실행
