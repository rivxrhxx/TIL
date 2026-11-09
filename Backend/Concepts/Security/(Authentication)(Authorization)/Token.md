# Token

토큰 기반 인증

서버는 인증된 유저에게 암호화된 토큰(사용자의 정보포함)을 발행하고 클라이언트에서 데이터를 보관하다가 서버로 요청할때 토큰 정보를 실어보내 인증하는 방식이다

- 인증 할때마다 DB를 확인하지않아 **서버의 부담이 덜** 하다.

## 관련 개념

- [[Backend/Concepts/Security/(Authentication)(Authorization)/JWT|JWT]] — 토큰을 표현하는 형식의 한 예.
- [[Backend/Concepts/Security/(Authentication)(Authorization)/Session|Session]] — 인증 상태를 관리하는 방식을 비교하며 읽을 노트.
