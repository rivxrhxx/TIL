# DI (의존성 주입)

DI는 Dependency Injection(의존성 주입)을 줄인 표현

**의존**한다는 건 어떤 클래스가 다른 클래스를 사용한다는 뜻 (A가 B를 사용하면 A는 B에 의존)

DI는 이 의존하는 객체(B)를 A가 직접 생성하지 않고 **외부(스프링 컨테이너)에서 넣어주는 것**

[[IOC|IoC]]를 구현하는 대표적인 방법이 DI

- 객체를 주입받는 모습 (필드 주입)

```java
@Service
public class A {
	// A에서 B를 주입받음
	@Autowired // 스프링 컨테이너에 등록된 빈 중 B 타입을 찾아 주입하는 역할
	private B b;
}
```

[[IOC]] 노트의 일반적인 객체 생성 코드에서는 개발자가 직접 `new B()`로 객체를 생성했지만, 위 코드는 `B b;`라고 선언만 했을 뿐 직접 객체를 생성하지 않고 주입받고 있음

이유는 스프링 컨테이너가 객체를 만들어서 주입했기 때문

이때 주입받는 A와 주입되는 B 모두 스프링 컨테이너에 [[Bean-Concept|빈]]으로 등록되어 있어야 함

- 생성자 주입 (권장 방식)

```java
@Service
public class A {
	private final B b;

	public A(B b) { // 생성자가 하나면 @Autowired 생략 가능
		this.b = b;
	}
}
```

- `final`로 선언할 수 있어 객체가 생성된 뒤 의존 객체가 바뀌지 않음
- 의존 객체 없이는 A를 만들 수 없어서 주입을 빠뜨리는 실수를 막음
- 스프링 없이도 `new A(new B())`처럼 직접 넣을 수 있어 테스트가 쉬움
- Lombok의 [[@RequiredArgsConstructor]]를 쓰면 이 생성자를 자동으로 만들어줌

## 관련 개념

- [[Backend/Concepts/Core/Bean/SpringContainer|스프링 컨테이너]] — 빈을 생성하고 의존성을 주입하는 주체.
- [[Language/JAVA/Constructor|생성자]] — 생성자 주입에서 의존 객체를 매개변수로 받는 방법.
