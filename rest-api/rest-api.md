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

REST (Representational State Tranfer)는 소프트웨어 아키텍처 스타일로, 웹 기술 기반의 아키텍처를 정의하는 방식을 말한다.&#x20;

REST 아키텍처 스타일은 7개의 제약 조건을 가지고 있다.

### 제약 조건

1. Starting with the Null Style
2. Client-Server
3. Stateless
4. Cache
5. **Uniform Interface** (핵심)
6. Layered System
7. Code-On-Demand
