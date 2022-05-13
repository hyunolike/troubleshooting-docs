## 문제
- `@CreatedDate` 설정 후에도 업데이트 null되는 에러

## 해결
```java
@CreatedDate
@Column(name = "CREATED", nullable = false, updatable = false) ✔
private LocalDateTime created;
```

- `@Column` 부분에 추가적인 설정 후 정상 업데이트
