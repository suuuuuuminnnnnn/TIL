## REST란?

---

REST(Representational State Transfer)의 약자로 자원을 이름으로 구분하여 해당 자원의 상태를 주고받는 모든 것을 의미한다.

HTTP URI(Uniform Resource Identifier)를 통해 자원(Resource)을 명시하고, HTTP Method(POST, GET, PUT, DELETE, PATCH 등)를 통해 해당 자원(URI)에 CRUD Operation을 적용한다.

<aside>
💡

CRUD Operation이란?
Create(생성), Read(조회), Update(수정), Delete(삭제)를 모아서 일컫는 말이다

</aside>

### REST의 구성 요소

REST는 다음과 같은 3가자의 요소로 구성되어 있다

1. 자원(Resource): HTTP URI
    - 모든 자원에 고유한 ID가 존재하고, 이 자원은 Server에 저장된다.
    - 자원을 구분하는 ID는 ‘/groups/:group_id’와 같은 HTTP URI
    - Clinet는 URI를 이용하여 자원을 지정하고 해당 자원의 상태(정보)에 대한 조작을 Server에 요청한다.
2. 자원에 대한 행위(Verb): HTTP Method
    - HTTP 프로토콜의 Method를 사용한다.
    - HTTP 프로토콜은 GET, POST, PUT, DELETE와 같은 메소드를 제공한다.
3. 자원에 대한 행위의 내용(Repersentation): HTTP Message Pay Load
    - Client가 자원의 상태(정보)에 대한 조작을 요청하면 Server는 이에 적절한 응답(Representation)을 보낸다
    - REST에서 하나의 자원은 JSON, XML, TEXT, RSS 등 여러 형태의 응답을 받을 수 있다.

### REST의 장단점

장점

- HTTP 프로토콜의 인프라를 그대로 사용하므로 REST API 사용을 위한 별도의 인프라를 구출할 필요가 없다.
- HTTP 프로토콜의 표준을 최대한 활용하여 여러 추가적인 장점을 함께 가져갈 수 있게 해준다.
- HTTP 표준 프로토콜에 따르는 모든 플랫폼에서 사용이 가능하다.
- Hypermedia API의 기본을 충실히 지키면서 범용성을 보장한다.
- REST API 메시지가 의도하는 바를 명확하게 나타내므로 의도하는 바를 쉽게 파악할 수 있다.
- 여러 가지 서비스 디자인에서 생길 수 있는 문제를 최소화한다.
- 서버와 클라이언트의 역할을 명확하게 분리한다.

단점

- 표준이 자체가 존재하지 않아 정의가 필요하다.
- HTTP Method 형태가 제한적이다.
- 브라우저를 통해 테스트 할 일이 많은 서비스라면 쉽게 고칠 수 있는 URL보다 Header 정보의 값을 처리해야 하므로 전문성이 요구된다.
- 구형 브라우저에서 호환이 되지 않아 지원해주지 못하는 동작이 많다.

### REST의 특징

1. Server - Client(서버 - 클라이언트 구조)
2. Stateless(무상태성)
3. Cacheable(캐시 처리 가능)
4. Layered System(계층화)
5. Uniform Interface(인터페이스 일관화)