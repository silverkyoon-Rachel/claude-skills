---
name: component
description: 새로운 React 컴포넌트를 생성합니다. 적절한 폴더 구조와 타입을 포함합니다.
---

# Component 생성 스킬

새로운 React 컴포넌트를 생성합니다.

## 인자
$ARGUMENTS - 컴포넌트 이름 (예: UserCard, SalesChart)

## 1. 컴포넌트 위치 결정
- `components/ui/` - 기본 UI 컴포넌트 (Button, Input 등)
- `components/cards/` - 카드형 컴포넌트
- `components/charts/` - 차트 컴포넌트
- `components/layout/` - 레이아웃 컴포넌트
- `components/common/` - 공통 컴포넌트

## 2. 컴포넌트 템플릿
```tsx
import React from 'react';

interface ComponentNameProps {
  // props 정의
}

export const ComponentName: React.FC<ComponentNameProps> = ({
  // props 구조분해
}) => {
  return (
    <div>
      {/* 컴포넌트 내용 */}
    </div>
  );
};
```

## 3. 체크리스트
- [ ] Props 인터페이스 정의
- [ ] 적절한 폴더에 생성
- [ ] index.ts에 export 추가
- [ ] Tailwind 클래스 사용
- [ ] 반응형 고려 (sm, md, lg)

## 4. 생성 후
- 컴포넌트 파일 경로 안내
- 사용 예시 코드 제공

인자: $ARGUMENTS
