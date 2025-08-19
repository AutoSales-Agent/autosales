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
Agent(Express): http://localhost:3000