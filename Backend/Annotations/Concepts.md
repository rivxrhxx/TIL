# 어노테이션?

사전적으로 “주석” 의미를 가지고있다.

자바 코드에 메타데이터를 추가하여 컴파일러나 런타임에서 특정 동작을 유도한다.

한마디로 프로그램에게 추가적인 정보를 제공해주는 메타데이터라고볼수있음

## 대표적인 어노테이션 종류

|어노테이션|설명|
|---|---|
|@Override|부모 클래스나 인터페이스의 메서드를 재정의했음을 명시|
|@Deprecated|더 이상 사용하지 않는 코드임을 표시|
|@SuppressWarnings|컴파일 경고를 무시하도록 설정|
|@FunctionalInterface|함수형 인터페이스임을 명시|

## 관련 개념

- [[Language/JAVA/Override|오버라이딩]] — 본문의 대표 어노테이션 표에 등장하는 메서드 재정의.
- [[Backend/Annotations/lombok/Concepts|Lombok]] — 어노테이션으로 반복 코드를 생성하는 활용 예.
- [[Backend/Annotations/@PathVariable|@PathVariable]] — 웹 요청의 경로 변수를 다루는 어노테이션.
- [[Backend/Annotations/@Valid|@Valid]] — 입력 데이터 검증에 사용하는 어노테이션.
