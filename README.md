# 정윤환 (Jeong Yun-hwan)

### 백엔드 개발자 (Backend Developer)
대규모 트래픽 처리와 안정적인 분산 인프라 구축을 지향하는 백엔드 개발자 정윤환입니다.  
도메인 특성에 맞는 동시성 제어와 보안 계층 설계에 관심이 많습니다.

---

### 연락처 및 링크
- **Email**: yunbin0115@gmail.com
- **Blog**: https://younanee.tistory.com/
- **GitHub**: https://github.com/Yunan1101

---

### 학력 및 활동 (Education & Activities)
- **가비아 (Gabia)** | g-Cloud 기반 그룹웨어 개발자 양성 과정 (2026.04 ~ 2026.10 진행 중)
- **순천향대학교** | 컴퓨터공학과 학사 졸업 (2020.03 ~ 2026.02)
  - 졸업 평점: **4.23 / 4.5**
  - 전공 평점: **4.3 / 4.5**
- **병역**: 육군 병장 만기 전역

---

### 보유 기술

**Backend**
- Java, Spring Boot, JPA, Spring Cloud Gateway, Spring Security
- Python

**Message / Real-time**
- RabbitMQ
- WebSocket (STOMP)
  
**Infrastructure & Database**
- MySQL, Oracle, PostgreSQL

---

### 자격증 (Certifications)
- **정보처리기사** | 한국산업인력공단
- **SQLD (SQL Developer)** | 한국데이터산업진흥원
- **ADsP (데이터분석 준전문가)** | 한국데이터산업진흥원

---

### 프로젝트 (Projects)

#### Emergency Matching System (응급 환자-병원 실시간 매칭 시스템)
- **진행 기간:** 2026.04 ~ 2026.06 (2인 백엔드, 1인 CI/CD)
- **Repository:** [GitHub Link](https://github.com/Yunan1101/emergency-matching-backend)
- **요약:** 구급대원이 입력한 환자 위치 기반으로 인근 병원을 조회하고, 다수 병원 중 최초 수락 병원과 실시간 매칭하는 분산 시스템
- **주요 구현 내용:**
  - Spring Cloud Gateway 기반의 전역 필터 적용 기법으로 JWT 통합 인증/인가 및 라우팅 구조 설계
  - 다수 병원의 동시 수락 요청 시 데이터 정합성을 보장하기 위해 DB 병목이 없는 **JPA 낙관적 락(@Version)** 도입 및 예외 처리 구조 설계
  - RabbitMQ를 통한 비동기 이벤트 디커플링 및 WebSocket(STOMP) 채널별 인터셉터 권한 검증을 통한 도청 방지 보안 계층 구현
  - 외부 서비스(`hospital-service`) 단절을 대비해 **Feign Client Fallback** 구조를 도입하여 외부 장애 시에도 환자 접수 데이터가 보존되도록 시스템 가용성 확보
