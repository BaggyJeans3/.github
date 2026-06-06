<div align="center">

<img src="https://github.com/BaggyJeans3.png" width="130" />

<br/>
<sub>웹어플리케이션보안 · 캡스톤디자인</sub>

# 👖 BaggyJeans (배기진스)

중부대학교(고양캠퍼스) 정보보호학 전공 학부생 프로젝트

<br/>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

</div>

---

## 🍀 팀원

<div align="center">

| <img src="https://github.com/annseojin.png" width="72"> | <img src="https://github.com/progremer123.png" width="72"> | <img src="https://github.com/leeazyone.png" width="72"> | <img src="https://github.com/leetaeyeon11111.png" width="72"> | <img src="https://github.com/dodo4421.png" width="72"> |
|:---:|:---:|:---:|:---:|:---:|
| [@annseojin](https://github.com/annseojin) | [@progremer123](https://github.com/progremer123) | [@leeazyone](https://github.com/leeazyone) | [@leetaeyeon11111](https://github.com/leetaeyeon11111) | [@dodo4421](https://github.com/dodo4421) |
| 안서진 | 백이랑 | 이지원 | 이태연 | 장재원 |
| 팀장 | 팀원 | 팀원 | 팀원 | 팀원 |

</div>

---

## 📦 Projects

<div align="center">

| | Repository | Description |
|:---:|:---|:---|
| 🛡️ | **[Aegis-3](https://github.com/BaggyJeans3/Aegis-3)**<br/><sub>`Python` `Node.js` `FastAPI` `Celery` `Nginx+Coraza` `Docker` `Gemini`</sub> | `4-1 캡스톤디자인` · AI 기반 지능형 API 보안 게이트웨이 & SOAR 오케스트레이터 |
| 📊 | **[Aegis-3-Portal](https://github.com/BaggyJeans3/Aegis-3-Portal)**<br/><sub>`TypeScript`</sub> | `4-1 캡스톤디자인` · Aegis-3 관제·고객사 대시보드 프론트엔드 |
| 🔒 | **[aegis_project](https://github.com/BaggyJeans3/aegis_project)**<br/><sub>`Shell` `Python` `inotify` `cron` `Slack`</sub> | `4-1 취약점진단및평가` · KISA 기준 시스템 설정 파일 무결성 자동 감사·복구 |
| 🗳️ | **[blockchain-voting](https://github.com/BaggyJeans3/blockchain-voting)**<br/><sub>`TypeScript` `Next.js` `Solidity` `Hardhat` `Tailwind`</sub> | `3-2 캡스톤디자인` · 블록체인 기반 전자투표 플랫폼 ([baggyjeans.site](https://baggyjeans.site/)) |

</div>

---

### 🛡️ Aegis-3 — 지능형 API 보안 게이트웨이 & SOAR 오케스트레이터

들어오는 트래픽을 막고, 분석하고, 학습해 다음 공격을 자동 차단하는 통합 보안 플랫폼입니다.

- **WAF 방어** — Nginx + Coraza WAF + OWASP CRS + 자체 룰셋, L7 Rate Limit
- **개인정보 자동 마스킹** — 전화·주민번호·카드·이메일 정규식 실시간 치환 (2-pass 구조)
- **동적 보안 프록시** — Express + PostgreSQL 멀티테넌트 라우팅, 허니팟 유도
- **SOAR 파이프라인** — Redis 큐 + Celery Worker/Beat 비동기 위협 수집·정규화
- **Risk Score Engine** — SSRF·Command Injection 등 다중 detector로 위험도 0~100점 정량화
- **AI WAF 룰 생성기** — Google Gemini가 고위험 로그 분석 → PCRE 룰 자동 생성·주입·즉시 차단 (Shadow Mode 검증 + 하이브리드 TTL + 재무장)
- **실시간 대응** — Cloudflare IP 차단, Slack ChatOps, HTML 이메일 보고서
- **대시보드 백엔드** — FastAPI + Supabase JWT 인증, 테넌트 격리, SSE 스트림

`Python` `Node.js / Express` `FastAPI` `Celery` `Redis` `PostgreSQL` `MongoDB` `Docker Compose` `Nginx + Coraza WAF` `OWASP CRS` `Google Gemini` `Cloudflare` `Slack` `Supabase`

---

### 📊 Aegis-3-Portal — 관제 대시보드 프론트엔드

Aegis-3 백엔드(`aegis-portal-backend`)와 연동되는 웹 대시보드입니다. 관리자·고객사가 실시간 위협 로그·통계·이벤트 스트림을 조회하는 화면을 담당합니다. (Aegis-3가 데이터를 만들고, Portal이 보여주는 역할 분담)

`TypeScript`

---

### 🔒 aegis_project — 시스템 설정 무결성 감사·복구

`/etc/passwd`, `/etc/shadow`, `sshd_config` 등 핵심 시스템 파일의 무단 변조를 탐지하고 복구하는 방어 도구입니다. *(README 제목은 "Aegis-3"이지만 위 API 게이트웨이와는 별개의 Shell 기반 프로젝트)*

- **Audit / Target 2서버 구조** — 황금 기준선 보관 + 원격 교차 감사
- **3단 탐지 (Defense in Depth)** — 실시간 inotify + 주기 cron 해시 검증 + 원격 교차 검증 (Target 감시 무력화돼도 우회 불가)
- **관리자 승인 워크플로우** — Slack 알림 → RESTORE / KEEP / HOLD
- **완전 자동화** — `@reboot` 재가동, 헬스체크 자동 재시작, KEEP 후 기준선 자동 재구축, 매일 HTML/PDF 보고서

`Bash / Shell` `Python` `inotify-tools` `cron` `SSH / SCP` `Slack Webhook` `wkhtmltopdf · pdfkit`

---

### 🗳️ blockchain-voting — 블록체인 기반 전자투표 시스템

> 탈중앙화 · 무결성 · 익명성 · 접근성을 갖춘 온라인 투표 플랫폼 — 🔗 **[baggyjeans.site](https://baggyjeans.site/)**

"내 표가 올바르게 반영되었는가?"라는 신뢰 문제를, 누구나 검증 가능한 블록체인 기록으로 해결합니다.

- **이중 인증** — DID 또는 MetaMask 지갑 인증 (신원과 투표 데이터 분리로 익명성 유지)
- **스마트 컨트랙트** — Solidity 투표 생성·참여·집계 로직, EVM 네트워크(Sepolia 등) 연동
- **검증 가능성** — 주요 이벤트 온체인 기록 → 블록 익스플로러로 누구나 확인
- **보안 강화** — 관리자 수정/삭제 시 비밀번호 + DID/지갑 인증, 암호 복잡도 정책
- **모의 선거** — 학습·연구용 시뮬레이션 시나리오 지원

`TypeScript` `React` `Next.js` `Tailwind CSS` `Solidity` `Hardhat` `MetaMask` `DID` `Supabase` `EVM / Sepolia`

---

<div align="center">
<sub>
Python · TypeScript · Solidity · Node.js · FastAPI · Next.js<br/>
Celery · Redis · PostgreSQL · MongoDB · Supabase<br/>
Docker · Nginx + Coraza WAF · OWASP CRS · Google Gemini · Cloudflare · Slack · Hardhat
</sub>
</div>
