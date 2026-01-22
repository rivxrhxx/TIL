# JWT

Json Web Token 의 약자로 속성 정보 (Claim)를 Json 데이터 구조로 표현한 토큰으로서 네트워크를 통해서 서로 다른 장치끼리 안전하게 전송하기위해 설계됨

JWT는 세 파트로 나누어진다

헤더 (Header), 페이로드(payload), 서명 (Sinature)로 구성된다

1. Header : 해시 암호화 알고리즘과 토큰의 타입구성
2. Payload: 토큰에 담을 claim 정보를 포함
3. signature : Header Payload ,Secret key를 합쳐 암호화한 결과값