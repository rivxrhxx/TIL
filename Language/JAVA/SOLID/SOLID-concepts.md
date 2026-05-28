# SOLID

SOLID원칙이란 객체지향설게에서 지켜줘야할 5개의 소프트웨어 원칙이다

**(SRP , OCP , LSP , ISP ,DIP)**

합쳐서 SOLID

SRP(Single Responsibilty Principle) : 단일 책임 원칙

OCP(Open Closed Priciple): 개방 폐쇄 원칙

LSP(Listov Subsitution Priciple) : 리스코프 치환 원칙

ISP(Interface Segregation Principle) : 인터페이스 분리 원칙

DIP(Dependency Inversion Principle) : 의존 역전 원칙

SOLID 객체 지향 원칙을 적용하면 코드를 확장하고 유지 보수 관리하기가 쉬워진다 , 불필요한 복잡성을 제거해 리팩토링에 소요되는 시간을 줄임으로써 프로젝트 개발의 생산성을 높일수있다.
## **1. 단일 책임 원칙 (SRP : Single Responsibility Principle)**

- 클래스는 단 하나의 책임만 가져야 한다.
- 하나의 클래스는 하나의 기능만 담당해야 한다.
- 변경 이유도 하나여야 한다.

### **예시**

- 회원 저장 클래스 → 회원 저장만 담당
- 로그인 클래스 → 로그인 기능만 담당

---

## **2. 개방 폐쇄 원칙 (OCP : Open/Closed Principle)**

- 확장에는 열려 있어야 하고 수정에는 닫혀 있어야 한다.
- 새로운 기능 추가 시 기존 코드를 최대한 수정하지 않아야 한다.
- 기능은 확장으로 추가하고 기존 코드는 유지하는 것이 중요하다.

### **예시**

- 새로운 결제 방식 추가 시 기존 결제 코드는 수정하지 않고 새로운 클래스만 추가

---

## **3. 리스코프 치환 원칙 (LSP : Liskov Substitution Principle)**

- 자식 클래스는 부모 클래스를 대체할 수 있어야 한다.
- 부모 타입 자리에 자식 객체를 넣어도 프로그램이 정상 동작해야 한다.

### **예시**

- Bird 클래스의 fly()를 Penguin이 사용할 수 없다면 LSP 위반

---

## **4. 인터페이스 분리 원칙 (ISP : Interface Segregation Principle)**

- 인터페이스를 기능별로 작게 분리해야 한다.
- 사용하지 않는 기능까지 강제로 구현하게 하면 안 된다.

### **예시**

- 복합기 인터페이스를
    
    - 프린터 인터페이스
    - 스캐너 인터페이스  
        로 분리

---

## **5. 의존 역전 원칙 (DIP : Dependency Inversion Principle)**

- 구현 클래스가 아닌 추상화(인터페이스, 추상 클래스)에 의존해야 한다.
- 구체적인 객체보다 상위 개념에 의존하는 것이 중요하다.