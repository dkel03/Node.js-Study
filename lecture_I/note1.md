19.08.15

## Node.js : Event-driven, non-blocking IO, Single-Thread에 대하여

 - JavaScript 엔진은 single thread이다. 
- Node의 v8엔진도 single thread이다.
- Node system이 가진 libuv 라이브러리가 이벤트 루프를 제공한다.
- 자바스크립트 엔진은 비동기 작업을 위해 node.js의 api를 호출하며, 이때 넘겨진 콜백은 libuv의 이벤트 루프를 통해 스케쥴되고 실행된다.
- 자바스크립트가 '단일 스레드' 기반의 언어라는 말은 '자바스크립트 엔진이 단일 호출 스택을 사용한다'는 관점에서만 사실이다
- 실제 자바스크립트가 구동되는 환경(브라우저, Node.js등)에서는 주로 여러 개의 스레드가 사용되며, 이러한 구동 환경이 단일 호출 스택을 사용하는 자바 스크립트 엔진과 상호 연동하기 위해 사용하는 장치가 바로 '이벤트 루프'인 것이다.

