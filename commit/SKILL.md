---
name: commit
description: Git 커밋을 생성합니다. 변경사항을 확인하고 의미있는 커밋 메시지를 작성합니다.
---

# Git Commit 스킬

사용자가 커밋을 요청했습니다. 다음 단계를 따르세요:

## 1. 현재 상태 확인
```bash
git status
git diff --staged
git diff
```

## 2. 최근 커밋 스타일 확인
```bash
git log --oneline -5
```

## 3. 커밋 메시지 작성 규칙
- 첫 줄: 50자 이내, 동사로 시작 (Add, Fix, Update, Refactor, Remove 등)
- 빈 줄 후 상세 설명 (필요시)
- 마지막에 Co-Authored-By 추가

## 4. 커밋 실행
```bash
git add <파일들>
git commit -m "$(cat <<'EOF'
커밋 메시지

상세 설명 (필요시)

Co-Authored-By: Claude <noreply@anthropic.com>
EOF
)"
```

## 5. 결과 확인
```bash
git log -1
git status
```

## 주의사항
- .env, credentials 등 민감한 파일은 커밋하지 않음
- 사용자가 명시적으로 요청하지 않으면 push하지 않음
- 커밋 전 변경사항을 사용자에게 보여주고 확인

인자: $ARGUMENTS
