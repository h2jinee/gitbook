# 1⃣ REST API

## API(Application Programming Interface)

> API는 프로그래머가 소프트웨어 또는 서비스에서 데이터나 기능에 액세스 할 수 있는 방법을 정의한 것.
>
> 즉, API는 <mark style="color:purple;">**소프트웨어 간에 상호 작용할 수 있도록 만들어진 인터페이스**</mark>를 말한다.

## 정보은닉(Information Hiding)과 캡슐화(Encapsulation)

### 정보은닉이란?

> <mark style="color:purple;">**프로그램의 내부 구조와 구현 방식을 외부에서 감추고**</mark> 이를 외부에서 사용할 때 필요한 만큼의 정보만을 제공하는 것을 말한다. 정보은닉은 프로그램의 안전성, 유지보수성, 재사용성을 향상시키며, 프로그램을 외부에서 제대로 사용할 수 있도록 도와준다.

### 캡슐화란?

> <mark style="color:purple;">**정보은닉의 개념을 확장한 것**</mark>으로, 프로그램의 데이터와 그 데이터를 처리하는 로직을 하나의 단위(캡슐)에 묶어서 관리하는 것을 말한다. 캡슐화는 프로그램의 구조를 명확하게 구분하여 개발 및 유지보수가 용이하도록 하며, 외부에서의 불필요한 접근을 차단하여 프로그램의 내부 데이터를 안전하게 보호할 수 있다.

### 둘의 차이

아샬님께서 은닉은 뒤?에 숨는 것이라면 캡슐화는 감싸는 것이라고 하셨다.

근데 사실 완벽하게 이해가 되지 않는다..

추후에 다시 공부해야 될 것 같다.

## Architecture와 Architecture Style의 차이

Architecture는 <mark style="color:purple;">**소프트웨어 시스템의 구조, 구성, 관계, 동작 등을 설계하고 정의하는 것**</mark>을 말한다.

소프트웨어 시스템의 기능, 성능, 확장성, 유지보수성, 보안 등의 요구사항을 만족시키면서 구조와 관계를 결정한다.



Architecture Style은 <mark style="color:purple;">**소프트웨어 시스템의 구조를 표현하는 방법을 정의한 패턴**</mark>을 말하며,

소프트웨어 시스템의 구조를 일정한 형식으로 표현하고, 재사용 할 수 있는 패턴을 제공한다.

Model-View-Controller(MVC), Representational State Transfer(REST), Microservices 등이 그  예이다.

> <mark style="color:purple;">**결론적으로 Architecture는 소프트웨어 시스템의 구조를 설계하는 것,**</mark> \ <mark style="color:purple;">**Architecture Style은 구조를 표현하는 패턴을 말한다.**</mark>

## REST(7가지 제약 조건 위주로 정리)

<mark style="color:purple;">**REST (Representational State Tranfer)**</mark>는 소프트웨어 아키텍처 스타일로, 웹 기술 기반의 아키텍처를 정의하는 방식을 말한다.&#x20;

> <mark style="color:purple;">REST는 Representational State Tranfer의 약자로 해당 용어는 로이필딩에 의해 만들어졌다.</mark>

REST는 웹 서비스에서 많이 사용되는데, Application 사이에 결합도를 낮추게끔 설계하는 아키텍처 스타일이다. 결합도를 낮추기 위해 7가지 제약 조건을 가지고 있다.

### 제약 조건

1. Starting with the Null Style
2. Client-Server
3. Stateless
4. Cache
5. **Uniform Interface**
6. Layered System
7. Code-On-Demand

### Starting with the Null Style

아키텍처 설계 과정에 있어 두 가지 일반적인 관점이 있다.

첫 번째는 설계자는 아무 것도 없는 상태에서 설계를 시작하고, 시스템이 요구사항을 충족할 때까지 친숙한(familiar) 요소들을 이용해 아키텍처를 구성한다는 것이다.

두 번째는 설계자는 어떠한 제약 조건 없이 시스템의 전반에서 시작하여, 점진적으로 제약 조건을 추가한다는 것이다.

추가한 제약 조건들이 시스템 내에서 조화롭고 자연스럽게 동작할 수 있도록 설계를 진행해나간다.



첫 번째 관점은 <mark style="color:purple;">창의성(creativity)</mark>과 <mark style="color:purple;">무한한 비전(unbounded vision)</mark>을 강조하고,\
두 번째 관점은 시스템의 맥락에 대한 <mark style="color:purple;">이해(understanding)</mark>와 <mark style="color:purple;">규제(restraint)</mark>를 강조한다.



Null Sytle은 어떠한 제약 조건도 없는 상태이다. 아키텍처 설계의 관점에서 Null Style은 구성 요소간 경계가 없는 시스템을 말한다.



이것이 REST를 설명하기 위한 시작 조건이다.



이해가 가지 않아 다른 사이트에서 정리한 내용을 긁어 왔다.

[https://m.blog.naver.com/aservmz/222234406469](https://m.blog.naver.com/aservmz/222234406469)



### Client-Server

* 사용자들에게 제공하는 Interface인 User Interface와 데이터 스토리지, 알고리즘 등 서버 내부의 작업 들을 분리함으로써 User Interface는 여러 플랫폼에서의 이식성을 향상시킬 수 있으며, 서버는 그 구성요소를 단순화하여 확장성을 단순화 할 수 있다.
* 클라이언트와 서버가 서로 의존하지 않고 별도로 진화할 수 있다. 클라이언트는 서버의 리소스 URI만 알고 있으면 되기 때문!

### Stateless

* <mark style="color:purple;">**클라이언트에서 서버로의 각 요청에는 그 요청을 이해하는데 필요한 모든 정보가 포함**</mark>되어야 한다.\
  서버에 저장된 환경 정보를 이용해서 이득(서버에서의 클라이언트 정보 유지 등)을 취하면 안 된다.\
  따라서 세션의 정보는 전적으로 클라이언트가 가지고 있어야 한다.
* 로그인했다는 세션 유지가 필요하다면 그 정보 또한 Client가 해당 정보를 가지고 서버에 전달해야 한다. (JWT 등을 사용)

### Cacheable

* <mark style="color:purple;">**요청에 대한 응답 내의 데이터에 해당 요청은 캐시가 가능한지 불가능 한지 명시**</mark>해야 한다.\
  응답을 캐시할 수 있다면 클라이언트에서 동일한 요청이 왔을 때 응답 데이터를 재사용 할 수 있어야 한다.
* cache-control 헤더를 통하여 캐시 여부 명시

### Uniform Interface (핵심)

대체로 어렵지 않게 만족하지만, Uniform Interface를 만족하지 않는 경우가 많다.

#### Uniform Interface의 4가지  제약 조건 (필딩 제약 조건)

* identification of resources
  * URI 등으로 리소스를 식별할 수 있다.
* manipulation of resources through representations
  * 리소스 CRUD시에HTTP message에 표현을 담아 전송한다.
* <mark style="color:purple;">**self-descriptive message**</mark>
  * 메시지는 스스로를 설명해야 한다.
  * 메시지는 <mark style="color:purple;">자기서술적</mark>이기 때문에 여러 레이어에서 처리/변환 가능하다.
* <mark style="color:purple;">**hypermedia as the engine of application state (HATEOAS)**</mark>
  * 애플리케이션의 상태는 Hyperlink를 이용해 전이되어야 한다.

### Layered System

* <mark style="color:purple;">**계층화된 시스템 아키텍처를 사용하여 각 구성들 간의 계층을 마음대로 상호작용 할 수 없도록 제한**</mark>\
  함으로써 Interface를 일원화 할 수 있다.

### Code-On-Demand (optional)

* 서버가 네트워크를 통해 클라이언트에 전달한 javascript 등과 같은 프로그램들은 그 자체로 실행이 될 수 있어야 한다. 이것은 사전 구현에 필요한 기능의 수를 줄임으로써 클라이언트를 단순화한다.
* 우리가 평소에 정적인 데이터를 xml 또는 json에 담아서 client로 보내고, client가 이것을 가공한다.\
  하지만 <mark style="color:purple;">**code on demand라는 것은 client에 보내는 데이터를 바로 실행 가능한 코드를 보내서 이것을 Client에서 실행하는 것**</mark>을 말한다.
