---
name: chart
description: Recharts를 사용한 차트 컴포넌트를 생성합니다.
---

# Chart 생성 스킬

Recharts 라이브러리를 사용한 차트 컴포넌트를 생성합니다.

## 인자
$ARGUMENTS - 차트 유형 및 이름 (예: bar SalesChart, line TrendChart)

## 1. 지원 차트 유형
| 유형 | 컴포넌트 | 용도 |
|------|----------|------|
| bar | BarChart | 막대 그래프 |
| line | LineChart | 선 그래프 |
| area | AreaChart | 영역 그래프 |
| pie | PieChart | 파이 차트 |
| composed | ComposedChart | 복합 차트 |

## 2. 기본 템플릿 (Bar Chart)
```tsx
import React from 'react';
import { BarChart, Bar, XAxis, YAxis, CartesianGrid, Tooltip, Legend, ResponsiveContainer } from 'recharts';

interface ChartData {
  name: string;
  value: number;
}

interface ChartNameProps {
  data: ChartData[];
  title?: string;
}

export const ChartName: React.FC<ChartNameProps> = ({ data, title }) => {
  return (
    <div className="w-full h-[300px]">
      {title && <h3 className="text-lg font-semibold mb-2">{title}</h3>}
      <ResponsiveContainer width="100%" height="100%">
        <BarChart data={data}>
          <CartesianGrid strokeDasharray="3 3" />
          <XAxis dataKey="name" />
          <YAxis />
          <Tooltip />
          <Legend />
          <Bar dataKey="value" fill="#8884d8" />
        </BarChart>
      </ResponsiveContainer>
    </div>
  );
};
```

## 3. 색상 팔레트
```typescript
const COLORS = {
  primary: '#3b82f6',   // blue-500
  success: '#22c55e',   // green-500
  warning: '#f59e0b',   // amber-500
  danger: '#ef4444',    // red-500
  info: '#06b6d4',      // cyan-500
};
```

## 4. 체크리스트
- [ ] ResponsiveContainer 사용
- [ ] 적절한 색상 선택
- [ ] Tooltip 커스터마이징
- [ ] 데이터 타입 정의
- [ ] components/charts/에 생성
- [ ] index.ts에 export 추가

인자: $ARGUMENTS
