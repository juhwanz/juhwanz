<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=190&text=Hong%20Ju%20Hwan&fontSize=44&fontAlignY=36&desc=Backend%20Developer%20%C2%B7%20Java%20%2F%20Spring&descAlignY=58&animation=fadeIn" />

### Backend Developer

트랜잭션 정합성, 동시성, 장애 복구를
**코드와 테스트로 검증하는 백엔드 개발자**를 지향합니다.

<a href="https://github.com/juhwanz">
  <img src="https://img.shields.io/badge/GitHub-juhwanz-181717?style=flat-square&logo=github&logoColor=white"/>
</a>
<a href="mailto:ghdwnghks209@naver.com">
  <img src="https://img.shields.io/badge/Email-Contact-03C75A?style=flat-square&logo=naver&logoColor=white"/>
</a>

</div>

---

## 👋 About Me

* 🎓 강원대학교 컴퓨터공학과 졸업
* ☕ **Java / Spring 기반 Backend** 개발에 집중하고 있습니다.
* 단순 기능 구현보다 **정합성, 동시성, 트랜잭션 경계, 조회 성능, 장애 복구**를 고민합니다.
* 기술을 적용하는 것에서 끝내지 않고, **왜 선택했는지와 어떤 한계가 있는지** 설명할 수 있도록 기록합니다.
* 프로젝트의 문제를 `Problem → Constraints → Decision → Implementation → Verification → Trade-off` 흐름으로 정리합니다.

---

# 🚀 Featured Projects

## 🛒 E-Shop

> **동시 주문의 재고 정합성과 주문 폭주 상황의 조회 가용성을 함께 다루는 이커머스 백엔드 프로젝트**

<div>

![Java](https://img.shields.io/badge/Java-21-E76F00?style=flat-square\&logo=openjdk\&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3-6DB33F?style=flat-square\&logo=springboot\&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square\&logo=mysql\&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-Redisson-DC382D?style=flat-square\&logo=redis\&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square\&logo=docker\&logoColor=white)

</div>

### 핵심 문제

* 같은 상품에 주문이 몰려도 **초과 판매가 발생하지 않도록 재고 정합성 보장**
* 락 경합으로 인해 일반 상품 조회까지 영향을 받는 상황 완화
* 네트워크 재시도에 의한 **중복 주문 방지**
* 트래픽 증가에 따른 깊은 페이지 조회와 캐시 정합성 문제 개선

### 주요 구현

* 상품 단위 **Redisson Distributed Lock**
* Redis `SET NX` 기반 **Idempotency**
* Redis ZSet 기반 주문 **대기열**
* Transaction `AFTER_COMMIT` 기반 **Cache Invalidation**
* QueryDSL **No-Offset Pagination**
* Hibernate Batch Fetch 기반 N+1 완화
* GitHub Actions 빌드 검증 및 **Secret Scan**

### Links

[![Repository](https://img.shields.io/badge/Repository-E--Shop-181717?style=for-the-badge\&logo=github)](https://github.com/juhwanz/eshop-refac)
[![Architecture](https://img.shields.io/badge/Docs-Architecture-4285F4?style=for-the-badge)](https://github.com/juhwanz/eshop-refac/blob/main/docs/architecture.md)
[![Testing](https://img.shields.io/badge/Docs-Testing-25A162?style=for-the-badge)](https://github.com/juhwanz/eshop-refac/blob/main/docs/testing.md)

---

## 🎂 CakeShop

> **상품 탐색부터 주문·결제·픽업까지 구현한 팀 커머스 프로젝트 — 주문·결제 도메인 담당**

<div>

![Java](https://img.shields.io/badge/Java-21-E76F00?style=flat-square\&logo=openjdk\&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-4-6DB33F?style=flat-square\&logo=springboot\&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=flat-square)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square\&logo=mariadb\&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square\&logo=flyway\&logoColor=white)

</div>

### 담당 영역

**Order / Payment**

### 핵심 문제

* 클라이언트가 전달한 결제 금액을 그대로 신뢰할 수 없는 문제
* 주문·결제·재고·쿠폰 사이의 **상태 정합성**
* 중복 결제 승인과 결제 만료 경합
* 외부 PG 승인 이후 내부 처리 실패 시 발생하는 **부분 실패**
* 외부 시스템과 로컬 DB 사이의 일관성을 어떻게 회복할 것인가

### 주요 구현

* 상품·옵션·쿠폰 데이터를 이용한 **서버 금액 재계산**
* Order / Payment 상태 분리와 **State Transition**
* 재고·결제·주문·쿠폰을 묶는 Transaction 처리
* Toss Payments 승인·조회·취소 연동
* 중복 승인 방지를 위한 **Idempotency**
* 승인 이후 내부 실패에 대한 **보상·복구 흐름**
* Testcontainers 기반 MariaDB 통합 테스트
* Flyway 기반 스키마 관리

### Links

[![Personal Repository](https://img.shields.io/badge/Personal_Improvement-cakeshop__PV-181717?style=for-the-badge\&logo=github)](https://github.com/juhwanz/cakeshop_PV)
[![Team Repository](https://img.shields.io/badge/Team-cakeshop-181717?style=for-the-badge\&logo=github)](https://github.com/team-sweethan/cakeshop)

---

# 🛠 Tech Stack

### Backend

![Java](https://img.shields.io/badge/Java-21-E76F00?style=flat-square\&logo=openjdk\&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square\&logo=springboot\&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square\&logo=springsecurity\&logoColor=white)
![Hibernate](https://img.shields.io/badge/JPA-Hibernate-59666C?style=flat-square\&logo=hibernate\&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=flat-square)

### Database & Cache

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square\&logo=mysql\&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square\&logo=mariadb\&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square\&logo=redis\&logoColor=white)
![QueryDSL](https://img.shields.io/badge/QueryDSL-0769AD?style=flat-square)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square\&logo=flyway\&logoColor=white)

### Infra & Quality

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square\&logo=docker\&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square\&logo=amazonaws\&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square\&logo=githubactions\&logoColor=white)
![JUnit5](https://img.shields.io/badge/JUnit5-25A162?style=flat-square\&logo=junit5\&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-2496ED?style=flat-square\&logo=docker\&logoColor=white)

---

# 🎯 What I Focus On

| Area              | 관심사                                                        |
| ----------------- | ---------------------------------------------------------- |
| **Correctness**   | Transaction · Concurrency · Idempotency · State Transition |
| **Performance**   | SQL · Index · Pagination · Cache                           |
| **Reliability**   | Failure Recovery · Testing · CI · Observability            |
| **Architecture**  | Transaction Boundary · Domain Boundary · Trade-off         |
| **Collaboration** | Issue · PR · Code Review · Documentation                   |

---

# 📚 Engineering Approach

```text
문제를 먼저 정의합니다.
        ↓
제약조건과 실패 시나리오를 확인합니다.
        ↓
가능한 해결 방법을 비교합니다.
        ↓
기술을 선택하고 구현합니다.
        ↓
테스트와 측정으로 검증합니다.
        ↓
선택의 한계와 Trade-off를 기록합니다.
```

---

# 📊 GitHub

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=juhwanz&show_icons=true&hide_border=true&hide_title=true&include_all_commits=true" height="160" />

</div>

---

## 📫 Contact

<div align="center">

**Hong Ju Hwan**

Backend Developer · Java / Spring

[![GitHub](https://img.shields.io/badge/GitHub-juhwanz-181717?style=for-the-badge\&logo=github)](https://github.com/juhwanz)
[![Email](https://img.shields.io/badge/Email-Naver-03C75A?style=for-the-badge\&logo=naver\&logoColor=white)](mailto:ghdwnghks209@naver.com)

</div>
