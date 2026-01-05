# @Validated 후 알 유?

스프링 프레임워크가 지원하는 **검증 기능**의 핵심 어노테이션이다.

데이터가 들어왔을때 불량**(비어있거나 ,이상한값)**을 보내면 걸러서 보내줌

DTO나 Entity 규칙 (Notblank,Column)등등 붙혀놔도 검사하는 Validated가 없으면 **아무일도 일어나지않음**

# 예시

### Controller

```java
    @PostMapping("/create")
    @ResponseStatus(HttpStatus.CREATED)
    public void createGemini(@RequestBody @Validated GeminiRequest geminiRequest) {
        geminiCreateService.createGemini(geminiRequest);
    }
//validated 사용함
```

### Entity

```java
public class BoardEntity {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    public Long id;

    @Column(nullable = false)// <---이런거 잡아줌
    public String title;

    @Column(nullable = false)// <---이런거 잡아줌
    public String context;
}
```