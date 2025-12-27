# @AllArgsConstructor 넌 누구니?

간단하게 말하자면 **모든 필드값을 파라미터로 받는** 생성자를 생성

@AllArgsConstructor는 클래스의 모든 필드값을 파라미터로 받는 생성자를 자동으로 생성함

이 어노테이션을 사용하면 모든 필드를 한번에 초기화 할수있다

## 코드 예시

```java
import lombok.AllArgsConstructor;

@AllArgsConstructor
public class MyClass {
    private String name;
    private int age;
    private boolean active;
    
    // 롬복이 자동으로 생성하는 생성자:
    // public MyClass(String name, int age, boolean active) {
    //     this.name = name;
    //     this.age = age;
    //     this.active = active;
    // }
} 
```

### 사용목적?

주로 객체 생성시 모든 필드를 **초기화하는 경우나 의존성주입 ,DTO ,VO**등의 클래스를 초기화할때 유용함
