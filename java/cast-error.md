## 문제
- `...cannot be cast to java.lang.Integer`

## 해결
```java
//오류 발생
int num = (Integer) map.get("bno");

//우선 해당 오브젝트를 String으로 변환한 후 Integer.parseInt
int num = Integer.parseInt(String.valueOf(map.get("bno")));
```
