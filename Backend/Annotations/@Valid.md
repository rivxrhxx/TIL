# @Valid 너 누구야

Valid 유효성 검사를하는 어노테이션임

유효성 검사란 데이터가 요구하는 형식 (or 양식)에 맞는지 체크하는 검사이다

### @Valid 종류

|Annotaion|제약조건|
|---|---|
|@NotNull|Null 불가|
|@Null|Null만 입력 가능|
|@NotEmpty|Null, 빈 문자열 불가|
|@NotBlank|Null, 빈 문자열, 스페이스만 있는 문자열 불가|
|@Size(min=,max=)|문자열, 배열등의 크기가 만족하는가?|
|@Pattern(regexp =)|정규식을 만족하는가?|
|@Max(숫자)|지정 값 이하인가?|
|@Min(숫자)|지정 값 이상인가|
|@Future|현재 보다 미래인가?|
|@Past|현재 보다 과거인가?|
|@Positive|양수만 가능|
|@PositiveOrZero|양수와 0만 가능|
|@Negative|음수만 가능|
|@NegativeOrZero|음수와 0만 가능|
|@Email|이메일 형식만 가능|
|@Digits(integer=, fraction = )|대상 수가 지정된 정수와 소수 자리 수 보다 작은가?|
|@DecimalMax(value=)|지정된 값(실수) 이하인가?|
|@DecimalMin(value=)|지정된 값(실수) 이상인가?|
|@AssertFalse|false 인가?|
|@AssertTrue|true 인가?|

```java
implementation 'org.springframework.boot:spring-boot-starter-validation'
//해당 의존성이 있어야 사용가능 
```

여기서 Body는 보통 JSON값으로 들어오는데 변수가 1~2개일경우는 Requestparam으로

받아도되지만 몇십개 몇백개가 될수도있기에 별도의 Class타입으로 처리한다

-이것을 **DTO파일이라하는데** @RequstBody을 앞에붙혀주면된다.

```java
public ResponseEntity<Void> updateNotice(@PathVariable Long id, @Valid @RequestBody NoticeUpdateRequest request)
```