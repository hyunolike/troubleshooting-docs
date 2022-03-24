## 문제
- `IOException parsing XML document from class path resource` 에러 발생 ㅠ,ㅠ

`main.java`
```java
public class Driver {
    public static void main(String[] args) {
        ApplicationContext context = new ClassPathXmlApplicationContext("/export002.xml"); ⭐

        Car car = context.getBean("car", Car.class);
        Tire tire = context.getBean("tire", Tire.class);
        car.setTire(tire);
        System.out.println(car.getTireBrand());
    }
}
```

`설정.xml`
```java
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans http://www.springframework.org/schema/beans/spring-beans.xsd">
    <bean id="tire" class="com.heaven.mvc.expertspring30.KoreaTire"></bean>
    <bean id="americaTire" class="com.heaven.mvc.expertspring30.AmericaTire"></bean>
    <bean id="car" class="com.heaven.mvc.expertspring30.Car"></bean>

</beans>
```
## 해결
- `xml` 파일을 `resource` 패키지에 넣는다.
- 주의 사항 > 빈 설정 시 클래스 경로는 해당 패키지 경로를 그대로 써준다.

![image](https://user-images.githubusercontent.com/61215550/159830357-3f8eb87f-476a-45f2-97b9-33f345a5dffa.png)
