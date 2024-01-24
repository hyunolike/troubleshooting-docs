## 문제
- Long 자료형 계산하면 `0`으로만 나오는 문제
## 해결
> [참고자료](https://gist.github.com/singun/ad10e770a68ea54f9067) <br />
> [참고자료22](https://wotres.tistory.com/entry/java-%EC%88%AB%EC%9E%90-%EB%82%98%EB%88%84%EA%B8%B0-%EC%86%8C%EC%88%98%EC%A0%90-%EC%B6%9C%EB%A0%A5%ED%95%98%EB%8A%94-%EB%B2%95)
- ⭐곱셈연산 > int 자료형끼리 이루어짐
  - 오버플로 발생!
- 자바 타겟 타이핑 지원 x
- 결과 long > 피연산자들이 long이 아니면 long 연산 하지 않음!
- 🔥 나눗셈 소숫점 결과값 나오게 하는 방법
  - 피연산자 하나를 `double` 자료형으로 바꿔준다!

```java
🔥 자료형 나눗셈 주의
[문제 예시]
public class HelloWorld{
     public static void main(String []args){
        final long MICROS_PER_DAY = 24 * 60 * 60 * 1000 * 1000;
        final long MILLIS_PER_DAY = 24 * 60 * 60 * 1000;
        System.out.println(MICROS_PER_DAY / MILLIS_PER_DAY);
     }
}

[해결 예시]
public class HelloWorld{
     public static void main(String []args){
        final long MICROS_PER_DAY = 24l * 60 * 60 * 1000 * 1000;
        final long MILLIS_PER_DAY = 24l * 60 * 60 * 1000;
        System.out.println(MICROS_PER_DAY / MILLIS_PER_DAY);
     }
}

🔥 나눗셈 소수점 결과 나오게 하는 방법
class CodeRunner{
	public static void main(String[] args){
        	double value = 1/3d;
        	System.out.println(value);
	}
}

class CodeRunner{
	public static void main(String[] args){
        	double value = 1/3.0;
        	System.out.println(value);
	}
}
```
- 곱셈이 되는 첫번째 int를 `long` 으로 변경!
