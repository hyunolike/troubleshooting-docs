## 문제
- `mockMvc.perfrm(get())`에서의 `get(), post() ...` 함수를 못가져오는 문제

## 해결 
- 직접 `import` 한다!

```java
import static org.springframework.test.web.servlet.result.MockMvcResultMatchers.*;
import static org.springframework.test.web.servlet.request.MockMvcRequestBuilders.*;
```
