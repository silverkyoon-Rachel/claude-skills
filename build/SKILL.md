---
name: build
description: 프로젝트를 빌드하고 에러를 확인합니다.
---

# Build 스킬

프로젝트를 빌드하고 에러가 있는지 확인합니다.

## 1. 빌드 실행
```bash
cd figma-dashboard
npm run build
```

## 2. 결과 분석
- 빌드 성공 시: 빌드 시간, 번들 크기 안내
- 빌드 실패 시: 에러 원인 분석 및 수정 방안 제시

## 3. 일반적인 에러 유형
| 에러 | 해결 방법 |
|------|-----------|
| Type error | 타입 정의 확인/수정 |
| Import error | 경로 및 export 확인 |
| Module not found | 패키지 설치 확인 |
| Syntax error | 문법 오류 수정 |

## 4. 빌드 실패 시
1. 에러 메시지 분석
2. 관련 파일 확인
3. 수정 제안
4. 재빌드

## 5. 빌드 성공 시
```bash
# 번들 분석 (선택)
npm run build -- --analyze
```

인자: $ARGUMENTS
