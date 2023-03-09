## 문제 
- `현호.장.학교` 해당 문자열 `.` 마침표로 구분안되는 문제

## 해결
> [참고자료](https://hianna.tistory.com/618)

```java
String[] strArr = str.split("[.]");
String[] strArr = str.split("\\.");

배열 문자열 출력 방법 >> Arrays.toString(strArr)
```


### str.split("[.]")
- 정규식 `[ ]` >> 문자의 집합이나 범위를 뜻함

### str.split("\\.")
- 규식에서 역슬래시(\) 다음에 마침표와 같은 특수문자(즉, 정규식에서 특정한 의미를 가지는 문자)가 오면 역슬래시(\) 다음에 오는 문자를 일반 문자로 취급합니다.
