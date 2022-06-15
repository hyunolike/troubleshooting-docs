## 문제
- SSH를 통한 원격 서버 연결 명령어 실행 후 아래와 같은 에러 문구 나옴
- `packet_write_wait`

## 해결
> [참고 자료](https://musclebear.tistory.com/28)
- SSH 연결 후 아무동작 없을 시 이후에 pipe 에러 종료
- SSH 클라이언트(터미널)과 서버와의 상호작용을 하지 않을 때 발생
- 추가 동작 명령어를 작성하면 에러 해결됨.
