<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=190&section=header&text=Hong%20Ju%20Hwan&fontSize=46&fontAlignY=35&desc=Backend%20Developer%20%C2%B7%20Java%20%2F%20Spring&descAlignY=56&animation=fadeIn" width="100%" />

### Backend Developer

**트랜잭션 정합성 · 동시성 · 실패 복구를 코드와 테스트로 검증합니다.**

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
- ☕ **Java / Spring 기반 백엔드 개발**에 집중하고 있습니다.
- 기능 구현을 넘어 트랜잭션 경계, 동시성, 멱등성, 조회 성능과 실패 복구를 함께 설계합니다.
- 기술 선택을 `문제 → 제약과 실패 시나리오 → 선택 → 구현 → 검증 → Trade-off`의 흐름으로 기록합니다.

---

## 🚀 Featured Projects

### 🛒 E-Shop

> **고트래픽 주문 환경의 재고 정합성·멱등성·상품 단위 대기열을 검증하는 Spring Boot 백엔드 PoC**

![Java](https://img.shields.io/badge/Java-21-E76F00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-Hibernate-59666C?style=flat-square&logo=hibernate&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-11.8-003545?style=flat-square&logo=mariadb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-Redisson-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

| 관점 | 설계와 검증 |
|---|---|
| **Correctness** | 상품 단위 Redisson 분산 락, DB 재고 제약, Redis + DB 유일 제약 기반 주문 멱등성 |
| **Availability** | 락 대기를 트랜잭션 밖에 두어 DB 커넥션 점유를 줄이고, Redis ZSet 대기열로 상품별 진입 제어 |
| **Consistency** | 트랜잭션 `AFTER_COMMIT` 이벤트 기반 상품 캐시 무효화 |
| **Performance** | QueryDSL Offset Page / No-Offset Slice 분리, Hibernate Batch Fetch 적용 |
| **Evidence** | Testcontainers 동시성·통합 테스트, 반복 가능한 k6 baseline, GitHub Actions와 Gitleaks |

<p>
  <a href="https://github.com/juhwanz/eshop-refac"><img src="https://img.shields.io/badge/Repository-E--Shop-181717?style=for-the-badge&logo=github" /></a>
  <a href="https://github.com/juhwanz/eshop-refac/blob/main/docs/architecture.md"><img src="https://img.shields.io/badge/Docs-Architecture-4285F4?style=for-the-badge" /></a>
  <a href="https://github.com/juhwanz/eshop-refac/blob/main/docs/testing.md"><img src="https://img.shields.io/badge/Docs-Testing-25A162?style=for-the-badge" /></a>
  <a href="https://github.com/juhwanz/eshop-refac/blob/main/docs/load-testing.md"><img src="https://img.shields.io/badge/Docs-Load_Test-EF652A?style=for-the-badge" /></a>
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

| 관점 | 설계와 검증 |
|---|---|
| **Service Integrity** | 주문·결제 상태 전이, 결제 실패 복구, Spring Security 인증·인가 |
| **Architecture** | 기능별 수직 슬라이스와 명시적인 도메인 경계 |
| **Database** | Flyway migration으로 스키마 이력 관리 |
| **Testing** | MariaDB Testcontainers 통합 테스트와 GitHub Actions 빌드 검증 |
| **Storage** | 공통 저장소 계약과 AWS SDK for Java v2 기반 S3 연동 |

<p>
  <a href="https://github.com/juhwanz/cakeshop_PV"><img src="https://img.shields.io/badge/Personal_Improvement-cakeshop__PV-181717?style=for-the-badge&logo=github" /></a>
  <a href="https://github.com/team-sweethan/cakeshop"><img src="https://img.shields.io/badge/Team_Repository-cakeshop-181717?style=for-the-badge&logo=github" /></a>
</p>

---

## 🛠 Skills

| Area | Stack |
|---|---|
| **Backend** | Java 21 · Spring Boot · Spring Security · JPA / Hibernate · MyBatis · QueryDSL |
| **Data** | MariaDB · MySQL · Redis · Flyway |
| **Infra** | Docker · AWS S3 · GitHub Actions |
| **Quality** | JUnit 5 · Testcontainers · Gitleaks · k6 · ADR |

---

## 🧭 Engineering Approach

```text
Problem → Constraints & Failure Scenarios → Decision → Implementation → Verification → Trade-off
```

- 설계 주장은 실행 가능한 테스트와 재현 조건으로 뒷받침합니다.
- 운영에서 검증하지 않은 수치나 구성을 운영 성과로 과장하지 않습니다.
- Issue, PR, ADR과 문서로 선택의 이유와 다음 개선점을 남깁니다.
