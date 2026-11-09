# @NoArgsConstructor 무엇인가요

기본 생성자(매개변수가 없는 생성자) 를 생성한다

JPA나 ORM같은 프레임워크에서 엔티티를 생성하거나 빈 객체를 생성해야할때 사용됨

### 예시코드

```java
import lombok.NoArgsConstructor;

@NoArgsConstructor
public class MyClass {
    private String name;
    private int age;
    private boolean active;

    // 롬복이 자동으로 생성하는 생성자:
    // public MyClass() {
    // }
}
```

## 관련 개념

- [[Language/JAVA/Constructor|생성자]] — 매개변수가 없는 생성자의 의미.
- [[Backend/Concepts/JPA/JPA-Concepts|JPA]] — 본문에서 언급한 엔티티 생성과 기본 생성자의 관계.
