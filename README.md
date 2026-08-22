# 👋 안녕하세요, Backend Developer 이용현입니다.

Java와 Spring을 중심으로 백엔드 개발을 공부하고 있습니다.

단순한 CRUD 구현에 그치지 않고
**왜 이 기술이 필요한지, 어떤 문제를 해결하기 위해 사용하는지**를 이해하고
직접 프로젝트에 적용하는 과정을 중요하게 생각합니다.

Spring Boot 기반 서비스 개발을 시작으로
인증·인가, 데이터베이스, 캐시, 메시징, MSA, Docker 기반 배포와
Observability까지 백엔드 서비스의 전체 흐름을 넓혀가고 있습니다.

최근에는 **Redis, Kafka, MSA, Event-Driven Architecture, Observability, Resilience Pattern** 등
확장 가능하고 장애에 강한 서비스를 만들기 위한 기술을 학습하고 있습니다.

---

# 🛠 Tech Stack

## Backend

![Java](https://img.shields.io/badge/Java-17-007396?style=flat-square\&logo=openjdk\&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square\&logo=springboot\&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square\&logo=springsecurity\&logoColor=white)

* Java 17
* Spring Boot
* Spring MVC
* Spring Data JPA
* Hibernate
* Spring Security
* JWT
* Validation
* JPA Specification
* Pageable / Sort
* OpenFeign
* Spring AI
* Spring Cloud

---

## Database & Cache

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square\&logo=postgresql\&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square\&logo=redis\&logoColor=white)

* PostgreSQL
* Redis
* Caffeine Cache
* pgvector
* Soft Delete
* Transaction Management

---

## Messaging & Event

![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square\&logo=apachekafka\&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square\&logo=rabbitmq\&logoColor=white)

* Apache Kafka
* Kafka Producer / Consumer
* Consumer Group
* Event-driven Architecture
* Event Idempotency
* RabbitMQ Practice

---

## MSA & Spring Cloud

* Eureka Service Discovery
* Spring Cloud Config
* API Gateway
* OpenFeign
* Kafka-based Event Communication
* Service-to-Service Communication

---

## Infra & DevOps

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square\&logo=docker\&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square\&logo=amazonwebservices\&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square\&logo=githubactions\&logoColor=white)

* Docker
* Docker Compose
* AWS EC2
* Ubuntu
* SSH / SSH Tunnel
* GitHub Actions
* CI/CD
* Git / GitHub
* Feature Branch 기반 협업

---

## Observability

* Prometheus
* Grafana
* Loki
* Tempo
* Spring Boot Actuator
* Metrics / Logs / Traces

---

## AI & External API

* Spring AI
* Google Gemini API
* Slack API
* AI Prompt Design
* pgvector
* Vector Search 학습

---

## Test

* JUnit 5
* Mockito
* Spring Boot Test
* Testcontainers 경험
* Unit Test
* Integration Test

---

# 🚀 Representative Projects

## 🍽️ 1. Delivery

### AI 기반 음식 주문 관리 플랫폼

Spring Boot 기반으로
회원, 음식점, 메뉴, 장바구니, 주문, 결제, 리뷰, AI 기능을 구현한
**6인 팀 프로젝트**입니다.

🔗 [GitHub Repository](https://github.com/yonghyun0325/delivery)

### Tech Stack

`Java 17` `Spring Boot` `Spring Security` `JWT`
`Spring Data JPA` `PostgreSQL` `Caffeine Cache`
`Docker` `AWS EC2` `GitHub Actions` `Gemini API`

### My Role

* Review 도메인 구현
* ReviewReply 도메인 구현
* 주문 완료 후 리뷰 작성 검증
* 리뷰 등록 / 수정 / 삭제
* 리뷰 평균 평점 관리
* 리뷰 및 답글 권한 검증
* OWNER 실제 리소스 소유권 검증
* Soft Delete
* Swagger API 문서화
* Custom AccessDeniedHandler 구현
* Docker 기반 PostgreSQL 환경 구성
* AWS EC2 서버 구축 및 배포

### What I Learned

* 단순 Role 검증만으로는 부족하고
  **실제 리소스 소유권까지 검증해야 한다는 점**
* Entity를 외부에 직접 노출하지 않고 DTO를 통해 경계를 분리하는 방법
* 트랜잭션과 도메인 간 데이터 정합성 관리
* 팀 환경에서 Git Flow와 Feature Branch 기반으로 협업하는 방법
* 로컬 환경과 운영 환경의 차이
* Docker와 EC2를 이용한 실제 서비스 배포 흐름

---

## 🚚 2. Logistics Platform

### MSA 기반 물류 통합 관리 플랫폼

회원 승인, 허브, 업체, 주문, 배송, AI 알림까지
여러 서비스를 분리하여 구성한 **MSA 팀 프로젝트**입니다.

🔗 [GitHub Repository](https://github.com/LP-Team01/logistics-platform)

### Architecture

```text
Client
  ↓
API Gateway
  ↓
──────────────────────────────
User Service
Hub Service
Company Service
Delivery Service
AI Notification Service
──────────────────────────────
  ↓
Kafka / Redis / PostgreSQL
```

### Main Stack

`Java 17` `Spring Boot` `Spring Cloud`
`Eureka` `Config Server` `API Gateway`
`PostgreSQL` `Redis` `Kafka`
`Spring AI` `Gemini` `Slack API`
`Docker Compose` `GitHub Actions`

### My Role

**AI Notification Service 담당**

* AI 요청 도메인 구현
* 검색 조건 기반 동적 조회
* JPA Specification 활용
* Soft Delete
* Kafka Consumer 구현
* Delivery AI Notification Event 소비
* eventId 기반 중복 이벤트 방지
* 이벤트 데이터 검증
* 이벤트 버전 검증
* Gemini 기반 AI 처리
* Slack 알림 연동
* 일일 배송 경로 AI 알림 기능 구현
* Delivery Service 내부 통신을 위한 OpenFeign 적용
* 내부 서비스 인증 헤더 적용
* Kafka Consumer 테스트
* AI Event Mapper 테스트
* AI Notification Service 테스트
* Daily Route Prompt / Notification 테스트

### Event Flow

```text
Delivery Service
      ↓
    Kafka
      ↓
AI Notification Service
      ↓
    Gemini
      ↓
  Slack Notification
```

### What I Learned

* 서비스끼리 직접 호출하지 않고 Kafka Event를 이용해 결합도를 낮추는 방법
* Producer / Consumer / Topic / Consumer Group의 역할
* 중복 이벤트 소비 시 Idempotency가 필요한 이유
* 동기 통신과 비동기 이벤트 통신의 차이
* MSA에서 Config Server, Service Discovery, Gateway가 필요한 이유
* 외부 AI API와 비즈니스 로직을 연결하는 방법
* 서비스 간 내부 호출에서도 인증과 검증이 필요하다는 점

---

# 🔭 Observability Practice

## MSA Observability Mission

MSA 환경에서 장애를 단순히 로그만 보고 찾는 것이 아니라
**Metrics / Logs / Traces를 함께 활용하여 원인을 추적하는 방법**을 실습하고 있습니다.

### Stack

`Prometheus` `Grafana` `Loki` `Tempo` `Spring Boot Actuator`

### Practice

* Spring Boot Actuator Health Check
* JVM Memory Metrics 확인
* HTTP Request Metrics 확인
* Prometheus Metrics 수집
* Grafana Dashboard 확인
* Loki 기반 로그 분석
* Tempo 기반 Distributed Tracing
* 서비스 부하 테스트
* HTTP 500 Error 상황 확인
* Request Histogram 설정
* Rate Limiter 학습
* Backpressure 학습
* Bulkhead Pattern 학습

> Observability는 현재 학습 및 실습 단계이며,
> 운영 환경 경험으로 과장하지 않고 직접 실습한 범위만 정리하고 있습니다.

---

# 📚 Backend Learning Journey

백엔드 기술을 결과만 외우기보다
**웹 요청이 처리되는 가장 기본적인 구조부터 단계적으로 학습**하고 있습니다.

```text
Servlet / JSP
      ↓
Spring MVC
      ↓
Spring Boot
      ↓
Spring Data JPA
      ↓
Spring Security / JWT
      ↓
Redis
      ↓
Kafka
      ↓
MSA
      ↓
Observability
      ↓
Resilience / Distributed System
```

---

# 🧱 Legacy → Modern Backend

## 1. Servlet / JSP

🔗 [servlet-jsp-board](https://github.com/yonghyun0325/servlet-jsp-board)

* Servlet
* JSP
* JDBC
* Tomcat
* PostgreSQL
* WAR Deployment
* 게시판 CRUD
* Request / Response 흐름 학습

### Purpose

Spring을 사용하기 전에
웹 서버와 애플리케이션이 요청을 어떻게 전달하고
Servlet이 요청을 처리한 뒤 JSP가 화면을 반환하는지 이해하기 위해 진행했습니다.

---

## 2. Spring MVC + JSP

🔗 [spring-mvc-jsp-board](https://github.com/yonghyun0325/spring-mvc-jsp-board)

* Spring MVC
* Controller
* Service
* Repository
* JSP
* Tomcat
* PostgreSQL

### Purpose

Servlet에서 직접 처리하던 요청 흐름이
Spring MVC에서 어떻게 추상화되는지 비교하며 학습했습니다.

---

## 3. Spring Boot + JPA

🔗 [spring-boot-jpa-board](https://github.com/yonghyun0325/spring-boot-jpa-board)

* Spring Boot
* Spring Data JPA
* PostgreSQL
* REST API
* Entity / Repository / Service / Controller

### Purpose

JDBC 중심의 데이터 접근 방식에서
ORM 기반 데이터 접근 방식으로 발전하는 과정을 학습했습니다.

---

# ⚡ Redis Practice

Redis를 단순히 "빠른 DB"라고 이해하는 것보다
**어떤 데이터에 Redis가 적합한지 직접 구현하면서 학습**했습니다.

### Repositories

* [spring-redis-practice](https://github.com/yonghyun0325/spring-redis-practice)
* [redis-cache-practice](https://github.com/yonghyun0325/redis-cache-practice)
* [redis-session-clustering-practice](https://github.com/yonghyun0325/redis-session-clustering-practice)
* [redis-cart-session-practice](https://github.com/yonghyun0325/redis-cart-session-practice)
* [redis-leaderboard-practice](https://github.com/yonghyun0325/redis-leaderboard-practice)
* [redis-order-practice](https://github.com/yonghyun0325/redis-order-practice)

### Topics

* StringRedisTemplate
* Key / Value
* Set
* Cache
* TTL
* Session
* Session Clustering
* Shopping Cart
* Leaderboard
* 조회수
* 분산 환경에서의 상태 관리

### Learning Goal

기존 애플리케이션 내부 메모리 Cache와
분산 환경에서 사용할 수 있는 Redis의 차이를 이해하고 있습니다.

---

# 📨 Kafka Practice

Kafka의 Producer와 Consumer를 각각 분리하여
이벤트가 전달되는 과정을 직접 실습했습니다.

### Repositories

* [kafka-producer-practice](https://github.com/yonghyun0325/kafka-producer-practice)
* [kafka-consumer-practice](https://github.com/yonghyun0325/kafka-consumer-practice)

### Topics

* Producer
* Consumer
* Topic
* Broker
* Partition
* Consumer Group
* Event-based Communication
* Async Processing

### Learning Goal

```text
Service A
   ↓
 Kafka
   ↓
Service B
```

서비스가 서로 직접 의존하지 않고
Event를 통해 통신하는 구조와 장점을 이해하는 것을 목표로 했습니다.

---

# 🐇 RabbitMQ Practice

### Repositories

* [rabbitmq-product-practice](https://github.com/yonghyun0325/rabbitmq-product-practice)
* [rabbitmq-payment-practice](https://github.com/yonghyun0325/rabbitmq-payment-practice)

메시지 브로커를 이용해
서비스 간 비동기 통신 구조를 이해하기 위한 실습을 진행했습니다.

Kafka와 RabbitMQ를 단순히 같은 메시징 기술로 보지 않고
각 기술의 목적과 특성 차이를 이해하는 것을 목표로 하고 있습니다.

---

# 🔐 Authentication Practice

Spring Security와 인증 흐름을 별도로 학습하기 위한 프로젝트도 진행했습니다.

* [spring-auth](https://github.com/yonghyun0325/spring-auth)
* [sociallogin](https://github.com/yonghyun0325/sociallogin)

### Topics

* Authentication
* Authorization
* Spring Security
* JWT
* Social Login
* Role-based Authorization

---

# 🧠 What I Focus On

기술을 사용할 때 다음 네 가지를 정리하려고 합니다.

```text
1. 이 기술은 무엇인가?
2. 왜 필요한가?
3. 어떤 프로젝트에서 사용했는가?
4. 어떤 문제를 해결했는가?
```

예를 들어,

### Kafka

```text
What
분산 이벤트 스트리밍 플랫폼

Why
서비스 간 직접 의존성을 낮추고
비동기 처리를 하기 위해 사용

Where
Logistics Platform

Experience
Delivery 이벤트 Consumer
eventId 기반 중복 방지
AI Notification 처리
```

### Redis

```text
What
In-Memory Data Store

Why
빠른 데이터 접근과
분산 환경 상태 관리를 위해 사용

Where
Redis Practice / Backend Learning

Experience
Cache
Session
TTL
Leaderboard
Shopping Cart
```

---

# 🎯 Currently Learning

현재는 다음 주제들을 중심으로 학습하고 있습니다.

* MSA Architecture
* Event-driven Architecture
* Distributed System
* Redis
* Kafka
* Observability
* Resilience Pattern
* Rate Limiting
* Backpressure
* Bulkhead
* 장애 대응
* 성능 개선
* 테스트 전략

---

# 🌱 Development Direction

제가 지향하는 개발자는
**기능만 구현하는 개발자가 아니라 서비스가 왜 이렇게 설계되었는지 설명할 수 있는 개발자**입니다.

```text
"동작한다."
        ↓
"왜 동작하는지 안다."
        ↓
"왜 이 구조를 선택했는지 설명한다."
        ↓
"문제가 발생했을 때 원인을 찾고 개선한다."
```

백엔드 개발뿐 아니라
데이터베이스, 캐시, 메시징, 인프라, 모니터링까지 이해하며
서비스 전체 흐름을 볼 수 있는 개발자로 성장하고 있습니다.

---

# 📌 Selected Repositories

| Category         | Repository                                                                         | Description                 |
| ---------------- | ---------------------------------------------------------------------------------- | --------------------------- |
| Team Project     | [delivery](https://github.com/yonghyun0325/delivery)                               | Spring Boot 기반 AI 음식 주문 플랫폼 |
| MSA Team Project | [logistics-platform](https://github.com/LP-Team01/logistics-platform)              | MSA 기반 물류 통합 관리 플랫폼         |
| Redis            | [spring-redis-practice](https://github.com/yonghyun0325/spring-redis-practice)     | Spring + Redis 기본 실습        |
| Redis            | [redis-cache-practice](https://github.com/yonghyun0325/redis-cache-practice)       | Redis Cache 실습              |
| Kafka            | [kafka-producer-practice](https://github.com/yonghyun0325/kafka-producer-practice) | Kafka Producer 실습           |
| Kafka            | [kafka-consumer-practice](https://github.com/yonghyun0325/kafka-consumer-practice) | Kafka Consumer 실습           |
| Legacy Web       | [servlet-jsp-board](https://github.com/yonghyun0325/servlet-jsp-board)             | Servlet / JSP 게시판           |
| Spring MVC       | [spring-mvc-jsp-board](https://github.com/yonghyun0325/spring-mvc-jsp-board)       | Spring MVC + JSP            |
| Spring Boot      | [spring-boot-jpa-board](https://github.com/yonghyun0325/spring-boot-jpa-board)     | Spring Boot + JPA 게시판       |

---

# 📫 Contact

### GitHub

[@yonghyun0325](https://github.com/yonghyun0325)

---

### Thanks for visiting! 👋

계속 배우고, 직접 구현하고,
문제가 생겼을 때 원인을 설명할 수 있는 백엔드 개발자가 되겠습니다.
