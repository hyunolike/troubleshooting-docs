## 문제
- `R-studio` 에서 git push를 하던 중 발생했던 에러ㅠ,ㅠ
- `https` 클론을 진행해서 파일을 푸시하고자 하였다!

## 해결
- 클론 방식에 대한 이해 부족(아래 참고) 🤗
- `HTTPS` 방식으로 클론했기 때문에 SSH키가 아닌 `Windows Credential Store(자격증명 관리자)` 를 각각 계정정보를 저장하고 활용해야 됨
  - 매번 로그인할 필요가 사라진다
- 위 방식을 사용하지 않고 `remote add` 로 `ssh` 저장소를 추가해서 ssh키 인증 방식으로 푸시해 해결했다.✔
- ![image](https://user-images.githubusercontent.com/61215550/167250743-4ac04e97-2bb8-4a4b-83fd-99b9a7069be0.png)
- ![image](https://user-images.githubusercontent.com/61215550/167250748-357a883b-5838-41c2-8d09-8ac2ae540222.png)

### git 클론? `SSH` VS `HTTP`
> [참고 자료](https://develoduck.tistory.com/10)

- [Credential 저장소](https://git-scm.com/book/ko/v2/Git-%EB%8F%84%EA%B5%AC-Credential-%EC%A0%80%EC%9E%A5%EC%86%8C)
- [Git 서버-프로토콜](https://git-scm.com/book/ko/v2/Git-%EC%84%9C%EB%B2%84-%ED%94%84%EB%A1%9C%ED%86%A0%EC%BD%9C)
- `HTTPS`: Push, Pull 진행 시 사용자의 Username과 Password 물어봄
- `SSH`: SSH Key 인증 진행

### git - remote 리모트 저장소, 저장소 추가하는 법 
- 리모트 저장소: 인터넷이나 네트워크 어딘가에 있는 저장소
  - 저장소는 여러개 존재 가능! ✔
- 리모트 저장소 관리: 저장소를 추가, 삭제하는 것뿐아니라 브랜치 관리, 추적을 관리하는 거 
- `git remote` : 리모트 저장소 확인 
  - 처음 클론하면 자동으로 `origin` 으로 등록 
  - `git remote -v` : 단축이름 + URL 함께 보여줌
- 여러 사람들과 함께 관리하는 거면 아래와 같이 가능해진다

```
$ cd grit
$ git remote -v
bakkdoor  https://github.com/bakkdoor/grit (fetch)
bakkdoor  https://github.com/bakkdoor/grit (push)
cho45     https://github.com/cho45/grit (fetch)
cho45     https://github.com/cho45/grit (push)
defunkt   https://github.com/defunkt/grit (fetch)
defunkt   https://github.com/defunkt/grit (push)
koke      git://github.com/koke/grit.git (fetch)
koke      git://github.com/koke/grit.git (push)
origin    git@github.com:mojombo/grit.git (fetch)
origin    git@github.com:mojombo/grit.git (push)
```

- 리모트 저장소 추가 `git remote add hyunho https://github.com/hyunolike/naver`
