## 문제
- 깃 업데이트 이후, 깃랩 http 원격 저장소 이슈 나는 문제 


```
git -c diff.mnemonicprefix=false -c core.quotepath=false --no-optional-locks fetch --no-tags origin
fatal: Unencrypted HTTP is not supported for GitLab. Ensure the repository remote URL is using HTTPS.
remote: HTTP Basic: Access denied
```
## 해결
> 추측 >> 저장소 명 바뀌면서 생기는 문제? 깃 업데이트 문제? 최신 깃랩 문제?
- 소스트리 이용 `ssh` 저장소 경로로 수정
- ![image](https://github.com/hyunolike/troubleshooting-docs/assets/61215550/c983a3d3-d9a1-4b00-a8e8-5eb14b7a241e)
