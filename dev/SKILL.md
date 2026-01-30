---
name: dev
description: 개발 서버를 실행합니다.
---

# Dev 서버 스킬

Vite 개발 서버를 실행합니다.

## 1. 개발 서버 시작
```bash
cd figma-dashboard
npm run dev
```

## 2. 서버 정보
- 기본 URL: http://localhost:3000
- HMR (Hot Module Replacement) 지원
- 자동 새로고침

## 3. 문제 발생 시
| 문제 | 해결 |
|------|------|
| 포트 충돌 | 다른 포트 사용 `--port 3001` |
| 모듈 에러 | `npm install` 재실행 |
| 캐시 문제 | `node_modules/.vite` 삭제 |

## 4. 유용한 명령어
```bash
# 특정 포트로 실행
npm run dev -- --port 3001

# 네트워크 공개
npm run dev -- --host

# 캐시 클리어
rm -rf node_modules/.vite && npm run dev
```

인자: $ARGUMENTS
