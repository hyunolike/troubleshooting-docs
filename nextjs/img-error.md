## 문제
```
Unhandled Runtime Error
Error: Failed to parse src '이미지 파일명' on `next/image`, if using relative image it must start with a leading slash "/" or be an absolute URL (http:// or https://)
```

## 해결
- 경로 맨 앞에 `/` 이걸 안넣어서 발생한 휴먼에러 ㅋㅋㅋㅋㅋㅋㅋ


```ts
❌ 문제 발생 경로
images/markers/default.png

✅ 문제 해결 경로 - 앞에 / 이걸 넣어준다!
/images/markers/default.png
```
