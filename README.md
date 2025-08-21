# AutoSales Agent

B2B 세일즈 메일 자동화 시스템  
Spring Boot 백엔드 + Agentica(TypeScript) 에이전트 + MySQL + Redis 로 구성됨

---

## 📦 Prerequisites
- [Docker Desktop](https://www.docker.com/products/docker-desktop) 설치 (Windows / Mac / Linux 공통)

---

## 🚀 실행 방법

1. 소스 클론
```bash
git clone https://github.com/AutoSales-Agent/autosales.git
cd autosales-docker


2. 환경 변수 설정

프로젝트 루트(autosales-docker/)에 .env 파일을 에서아래 값 입력

DB_PASSWORD=change_me_root_pw

MAIL_USERNAME=
MAIL_PASSWORD=
OPENAI_API_KEY=sk-

COMPANY_NAME=DemoCorp
SENDER_NAME=홍길동

⚠️ MAIL_PASSWORD는 Gmail 보안 → 앱 비밀번호에서 생성해야 합니다.


3. 서비스 실행

docker compose up -d --build


4. 서비스 확인

Spring Boot (API 진입점): http://localhost:8080/chat

예시 프롬프트: 
1.카카오라는 회사를 등록해줘. 
  산업은 IT 플랫폼, 규모는 대기업이고, 
  담당자는 홍길동이고 이메일은 ex123@naver.com 이야. 
  언어는 한국어로 설정해줘.

2.클라우드 기반 보안 모니터링 프로젝트를 등록해줘. 
  산업은 IT 보안·클라우드 서비스야. 
  클라우드 환경에서 발생하는 침입 시도와 악성 트래픽을 AI가 탐지하고, 
  중소기업이 자체 보안 인력이 없어도 실시간으로 위협을 차단할 수 있도록 하는 서비스야.

3.카카오랑 클라우드 기반 보안 모니터링 프로젝트랑 연결해줘

4.클라우드 기반 보안 모니터링 프로젝트에 대해 카카오에게 제안메일 작성해줘


