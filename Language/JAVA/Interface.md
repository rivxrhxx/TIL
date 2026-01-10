# Java Interface(인터페이스)

다른 클래스를 작성하는경우 기본이되는 틀을 제공하면서 다른 클래스 사이의 **중간 매개 역할까지 담당**하는 일종 추상클래스를 의미한다.

간단한 예시

```java
//인터페이스 선언
public interface Animal{
	//추상 메소드 선언
	public void move();
}
```

```java
public class Dog implements Animal{
	//Animal의 추상 메소드 구현
	@Override
    public void move(){
    	System.out.println("개가 움직입니다.");
    }
}

//Cat 클래스 선언
public class Cat implements Animal{
	//Animal의 추상 메소드 구현
	@Override
    public void move(){
    	System.out.println("고양이가 움직입니다.");
    }
}
```

위 코드에서 Dog 와 Cat에게 제공하는 기본틀은 move() 라는 추상 메소드이다.

인터페이스는 클래스들이 공통적으로 구현해야할 메소드에대해 강제구현 의무를 구현한다.

한마디로.

**공통적으로 수행해야할 기본적인 기능을 인터페이스가 정의하여 제공한다는 말이다**