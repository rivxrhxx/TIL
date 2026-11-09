`@PreAuthorize` 어노테이션은 인증/인가 처리에서 사용하는 어노테이션으로 사용하려면 security config에 @EnableMethodSecurity 어노테이션이 필요하다
메서드가 호출하기전에 검사하여 실제로 해당메서드에 권한이있는지 판단한다.

## 관련 개념

- [[Backend/Concepts/Security/Concept|Spring Security]] — 메서드 권한 검사를 제공하는 보안 프레임워크.
- [[Backend/Concepts/Security/(Authentication)(Authorization)/Concepts|인증과 인가]] — 메서드 호출 전에 수행하는 인가의 의미.
