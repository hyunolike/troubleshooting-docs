## 문제 
- 아래와 같이 커멘드 연속으로 나열시 인식못하는 문제


```sh
echo "Hello, World!"
도커 mssql 명령어
```
## 해결
- 연속으로 나열하지 않고 줄띄어쓰기 하니까 정상적으로 동작


```sh
echo "Hello, World!"
✅ 빈 줄(띄어쓴거야)
도커 mssql 명령어
```
