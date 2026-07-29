# [비즈톡]

기업용 비즈메시지(카카오 알림톡 등) 발송 중계 서비스. 비즈메시지 발송·결과 처리 API와 고객사 대상 부가 서비스의 백엔드를 담당.

## 요약

- **기간**: 2022.10 - 2024.02
- **역할**: 백엔드 엔지니어
- **기술**: Spring Boot, Spring MVC, WebFlux, Spring Data JPA, MyBatis, Spring Security, Kafka, Redis, AWS S3, Jenkins, Thymeleaf/Bootstrap
- **주요 성과**
  - 비즈메시지 전송 요청을 처리하는 API 서버 개발·유지보수 및 Jenkins Pipeline 기반 CI/CD 구축
  - Kafka 이벤트 핸들링으로 발송·결과 데이터의 실시간 처리 성능 유지
  - 비즈메시지 이용 통계 조회 웹사이트를 1인 풀스택으로 전체 설계·개발
  - 발송 결과 Push 애플리케이션 백엔드 전체 개발 (Kafka Consumer + WebFlux 비동기 처리)
  - DB 과부하 지점을 Worker Application 분리·스케줄러 기반 파일 생성으로 개선

---

## 주요 프로젝트

### 비즈메시지 발송 및 결과 처리 API

- **기간**: YYYY.MM - YYYY.MM
- **사용기술**: Spring Boot, Kafka, Redis, AWS S3, Jenkins Pipeline, Slack Incoming Webhook
- **성과**: 비즈메시지 전송 요청 처리 API 서버의 개발·유지보수와 CI/CD·모니터링 체계 구축

비즈메시지 전송 요청을 처리하는 핵심 API 서버를 개발·유지보수했다.

- Kafka를 활용한 이벤트 핸들링·데이터 처리로 높은 실시간 처리 성능 유지
- 클라이언트 첨부파일의 AWS S3 스토리지 업로드 및 관리
- Redis로 반복 에러를 수집하고 Slack Incoming Webhook으로 실시간 알림하는 시스템 구현 — 장애 인지 시간 단축
- Jenkins Pipeline 기반 CI/CD 파이프라인 구축 및 관리

### 고객사 모니터링 서비스 — 비즈메시지 이용 통계 조회 웹사이트

- **기간**: YYYY.MM - YYYY.MM
- **사용기술**: Spring Boot, MyBatis, Spring Security, Thymeleaf, Bootstrap
- **성과**: 통계 조회 웹사이트를 1인 풀스택 프로젝트로 전체 설계·개발

고객사가 비즈메시지 이용 통계를 직접 조회할 수 있는 웹사이트를 혼자서 설계부터 개발까지 수행했다.

- RESTful API로 회원 관리, 통계 조회, 엑셀 출력 기능 구현
- 대량 통계 조회 시 DB 쿼리 과부하를 방지하기 위해 스케줄러 기반 파일 생성 방식으로 데이터 반환을 최적화

### 발송 결과 Push Application

- **기간**: YYYY.MM - YYYY.MM
- **사용기술**: Spring Boot, Kafka Consumer, Redis, WebFlux
- **성과**: 비즈메시지 발송 결과를 고객사에 Push 방식으로 전달하는 애플리케이션의 백엔드 전체 개발

- Kafka Consumer로 발송 결과를 수신하고 WebFlux 기반 비동기 처리로 실시간 전달 구현
- Redis를 결합해 처리 상태 관리 및 실시간 알림 기능 구성

### 비즈메시지 센터 API

- **기간**: YYYY.MM - YYYY.MM
- **사용기술**: Spring Boot, Spring MVC, Spring Data JPA, RestTemplate
- **성과**: 카카오 비즈메시지 발신용 프로필·템플릿 생성 API 서버 개발·유지보수, Worker 분리로 DB 부하 개선

카카오 비즈메시지 발신에 필요한 프로필과 템플릿을 생성하는 API 서버를 개발·유지보수했다.

- DB Insert/Select 과부하를 방지하기 위해 서버를 확장하고 쓰기 작업을 Worker Application으로 분리해 성능 개선

### 사내 출입현황 Application

- **기간**: YYYY.MM - YYYY.MM
- **사용기술**: Spring Boot, MyBatis
- **성과**: 출퇴근 시각 체크와 DB 조회/업데이트를 포함한 내부 관리 애플리케이션 개발

- 다중 DB Config 설정으로 복수 데이터베이스를 유연하게 관리하는 구성 적용
