# RabbitMQ 너 누군데

**RabbitMQ**는 **AMQP**를 따르는 오픈소스 **메시지 브로커**이다.
[[AMQP]]
메세지를 많은 사용자에게 전달하거나. 요청에 대한 처리 시간이 길때,

해당 요청을 다른 API에게 위임하고 **빠른응답**을 할 때 많이 사용한다.

또한, MQ를 사용하여 **애플리케이션 간 결합도**를 낮출수있는 장점도있다.

RabbitMQ에 중요한 개념으로는 크게 **Producer, Consumer, Queue, Exchange, Binding**이 있다.

### producer

- 메세지를 생성하고 발송하는 주체이다. 이 메세지는 큐에 저장되는데 주의할점은 Producer는 Queue에 직접 접근하지않고 항상 Exchange를 통해 접근한다.

### Consumer

- Consumer는 Queue에 직접 접근하여 메세지를 가져온다.

### Queue

- Producer들이 발송한 메세지들이 Consumer가 소비하기 전까지 보관되는 장소
- Queue는 이름으로 구분되는데 같은 이름과 다른 설정으로 Queue를 생성하려고 시도하면 에러가 발생한다.

### Exchange

- Producer들에게서 전달받은 메세지들을 어떤 Queue들에게 발송 할지를 결정하는 객체이다
- 네 가지 타입이있으며 일종의 라우터 개념이다.

### Binding

- exchange에게 메세지를 라우팅 할 규칙을 지정하는 행위
- 특정 조건에 맞는 메세지를 특정 큐에 전송하도록 설정할수있는데, 이는 해당 exChange타입에 맞게 설정되어야 한다.