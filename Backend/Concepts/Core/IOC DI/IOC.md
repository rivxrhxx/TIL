# IoC (제어의 역전)

IoC는 Inversion of Control(제어의 역전)을 줄인 표현

제어의 역전은 다른 객체를 직접 생성하거나 제어하는 것이 아닌

**외부에서 관리하는 객체를 가져와 사용하는 것**

즉 객체를 생성하고 의존관계를 관리하는 **제어권이 개발자의 코드에서 외부(스프링 컨테이너)로 넘어간다**는 의미

- 일반적인 객체 생성 : A가 사용할 B를 직접 생성

```java
public class A {
	private B b = new B(); // A가 B의 생성을 직접 제어
}
```

- 스프링 컨테이너가 객체를 관리하는 방식 : A는 B를 선언만 하고 생성은 외부에 맡김

```java
public class A {
	private B b; // 직접 생성하지 않음

	public A(B b) { // 외부에서 만들어진 B를 받아서 사용
		this.b = b;
	}
}
```

제어의 역전을 적용하면 객체를 외부에서 관리하게 되고, 실제로 사용할 때는 외부에서 제공해주는 객체를 받아오게 됨

객체를 생성하고 관리하는 주체를 [[SpringContainer|스프링 컨테이너]]라고 함

외부에서 객체를 넣어주는 구체적인 방법이 [[DI]](의존성 주입)

## 관련 개념

- [[Backend/Concepts/Core/Bean/Bean-Concept|Spring Bean]] — 스프링 컨테이너가 제어권을 갖고 관리하는 객체.
- [[Language/JAVA/SOLID/SOLID-concepts|SOLID]] — 구현 대신 추상화에 의존하라는 의존 역전 원칙(DIP)과 비교. 이름은 비슷하지만 IoC와는 다른 개념.
