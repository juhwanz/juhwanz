<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=210&section=header&text=Hong%20Ju%20Hwan&fontSize=46&fontAlignY=35&desc=Backend%20Developer%20%C2%B7%20Java%20%2F%20Spring&descAlignY=56&animation=fadeIn" width="100%" />

### Backend Developer

**트랜잭션 정합성 · 동시성 · 장애 복구 시나리오를 설계하고 테스트하는 백엔드 개발자를 지향합니다.**

<a href="https://github.com/juhwanz">
  <img src="https://img.shields.io/badge/GitHub-juhwanz-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>
<a href="mailto:ghdwnghks209@naver.com">
  <img src="https://img.shields.io/badge/Email-Contact-03C75A?style=for-the-badge&logo=naver&logoColor=white" />
</a>

</div>

---

## 👋 About Me

- 🎓 강원대학교 컴퓨터공학과 졸업
- ☕ **Java / Spring 기반 Backend** 개발에 집중하고 있습니다.
- 기능 구현에서 끝나지 않고 **트랜잭션 경계, 동시성, 멱등성, 조회 성능, 실패 복구**를 함께 고민합니다.
- 기술을 선택할 때 `문제 → 제약 → 선택 → 구현 → 검증 → Trade-off` 흐름으로 설명할 수 있도록 기록합니다.

---

## 🚀 Featured Projects

### 🛒 E-Shop

> **동시 주문의 재고 정합성과 주문 폭주 상황의 조회 가용성을 함께 다루는 이커머스 백엔드 프로젝트**

![Java](https://img.shields.io/badge/Java-21-E76F00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-Redisson-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**Key Engineering**

- 상품 단위 **Redisson 분산 락**과 트랜잭션 경계 분리
- Redis `setIfAbsent` 기반 **주문 멱등성 처리**
- Redis ZSet 기반 **주문 대기열 / 유량 제어**
- Transaction `AFTER_COMMIT` 기반 **상품 캐시 무효화**
- QueryDSL **Offset Page + No-Offset Slice** 조회 전략 분리
- Hibernate Batch Fetch 기반 주문 조회 최적화
- GitHub Actions 기반 빌드 검증 및 **Gitleaks Secret Scan**

<p>
  <a href="https://github.com/juhwanz/eshop-refac"><img src="https://img.shields.io/badge/Repository-E--Shop-181717?style=for-the-badge&logo=github" /></a>
  <a href="https://github.com/juhwanz/eshop-refac/blob/main/docs/architecture.md"><img src="https://img.shields.io/badge/Docs-Architecture-4285F4?style=for-the-badge" /></a>
  <a href="https://github.com/juhwanz/eshop-refac/blob/main/docs/testing.md"><img src="https://img.shields.io/badge/Docs-Testing-25A162?style=for-the-badge" /></a>
</p>

---

### 🎂 CakeShop

> **상품 탐색부터 주문·결제·픽업, 회원·커뮤니티·관리자 운영까지 연결한 팀 커머스 프로젝트**

![Java](https://img.shields.io/badge/Java-21-E76F00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-4.0.2-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=flat-square)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)

**Project Focus**

- 주문·결제 흐름과 **트랜잭션 / 상태 전이 / 결제 복구**를 포함한 서비스 무결성 설계
- Flyway 기반 **DB Migration** 관리
- MariaDB **Testcontainers 통합 테스트** 환경
- 기능별 수직 슬라이스와 명시적인 도메인 경계를 통한 협업 구조
- AWS SDK for Java v2 기반 **S3 스토리지 연동**
- Spring Security 기반 인증·인가 구성

<p>
  <a href="https://github.com/juhwanz/cakeshop_PV"><img src="https://img.shields.io/badge/Personal_Improvement-cakeshop__PV-181717?style=for-the-badge&logo=github" /></a>
  <a href="https://github.com/team-sweethan/cakeshop"><img src="https://img.shields.io/badge/Team_Repository-cakeshop-181717?style=for-the-badge&logo=github" /></a>
</p>

---

## 🛠 Tech Stack

### Backend
![Java](https://img.shields.io/badge/Java-21-E76F00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=flat-square)
![QueryDSL](https://img.shields.io/badge/QueryDSL-0769AD?style=flat-square)

### Data
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)

### Infra & Quality
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS-S3-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![JUnit5](https://img.shields.io/badge/JUnit5-25A162?style=flat-square&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-2496ED?style=flat-square&logo=docker&logoColor=white)

---

## 🎯 What I Focus On

| Area | Focus |
|---|---|
| **Correctness** | Transaction · Concurrency · Idempotency · State Transition |
| **Performance** | Query Optimization · Pagination · Cache |
| **Reliability** | Failure Recovery · Testing · CI |
| **Architecture** | Transaction Boundary · Domain Boundary · Trade-off |
| **Collaboration** | Issue · PR · Code Review · Documentation |

---

## 🧭 Engineering Approach

```text
Problem
  ↓
Constraints & Failure Scenarios
  ↓
Technical Decision
  ↓
Implementation
  ↓
Testing & Verification
  ↓
Trade-off & Next Improvement
```

---

## 📊 GitHub

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=juhwanz&show_icons=true&hide_border=true&hide_title=true&include_all_commits=true" height="160" />
</div>

---

<div align="center">

### 📫 Contact

**Hong Ju Hwan**  
Backend Developer · Java / Spring

<a href="https://github.com/juhwanz"><img src="https://img.shields.io/badge/GitHub-juhwanz-181717?style=for-the-badge&logo=github" /></a>
<a href="mailto:ghdwnghks209@naver.com"><img src="https://img.shields.io/badge/Email-Naver-03C75A?style=for-the-badge&logo=naver&logoColor=white" /></a>

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=120&section=footer" width="100%" />
