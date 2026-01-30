---
name: style
description: Tailwind CSS 스타일을 검토하고 개선합니다.
---

# Style 검토 스킬

Tailwind CSS 스타일을 검토하고 개선 사항을 제안합니다.

## 인자
$ARGUMENTS - 검토할 컴포넌트 또는 파일 경로

## 1. 스타일 검토 항목
- [ ] 반응형 디자인 (sm, md, lg, xl)
- [ ] 다크 모드 지원 (dark:)
- [ ] 호버/포커스 상태 (hover:, focus:)
- [ ] 일관된 spacing (p-, m-, gap-)
- [ ] 색상 일관성

## 2. 자주 사용하는 패턴

### 카드 스타일
```tsx
className="bg-white rounded-lg shadow-md p-6 hover:shadow-lg transition-shadow"
```

### 버튼 스타일
```tsx
className="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-colors"
```

### 그리드 레이아웃
```tsx
className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4"
```

### 플렉스 센터
```tsx
className="flex items-center justify-center"
```

## 3. 색상 시스템 (프로젝트 기준)
| 용도 | 클래스 |
|------|--------|
| 배경 | bg-slate-800, bg-white |
| 텍스트 | text-gray-900, text-slate-200 |
| 강조 | text-blue-500, bg-blue-500 |
| 성공 | text-green-500, bg-green-500 |
| 경고 | text-amber-500, bg-amber-500 |
| 위험 | text-red-500, bg-red-500 |

## 4. 개선 제안
- 반복되는 클래스 → 컴포넌트화
- 긴 클래스 목록 → cn() 유틸리티 사용
- 인라인 스타일 → Tailwind 클래스로 변환

인자: $ARGUMENTS
