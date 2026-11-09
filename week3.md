# Week 3 (11/09 ~ 11/13)

# 11/09/2026

## Variant 폭증
: 경우에 수마다 Variant를 만들면 Varient 개수가 곱셈으로 늘어남. 문구/아이콘까지 Variant로 만들면 관리하기 어려움. 그러나 개수가 많아지면 Component를 만드는 메인 이유 (수정을 쉽고 편리하게 하기 위한 shortcut)의 의미가 없어짐
=> 해결책: Variant + Property 섞어쓰기

### Types of Properties
1. Variant (모양/상태가 달라질 때)
e.g., Type=Primary, State=Disabled
2. Text (문구만 바뀔 때)
e.g., 예약하기 -> 대기 신청
3. Boolean (보일 것인가/숨길 것인가)
e.g., show=True
4. Instance Swap (같은 자리, 다른 element/부품)
e.g., icon/heart -> icon/check

이 Property를 각 Main Component's Instance의 Properties panel내에서 한번에 해당 Instance의 모든 Properties view/edit 가능하게
--> 한 Instance 당 Override 하기가 더 편리해짐

### Setting Properties 방법
**중요:** _Variant를 제외한_ 각 Property는 Layer마다 연결을 해야 작동 됨 (연결된 Property는 Layer Panel/Sidebar에서 보라색으로 바뀜)

#### 공통 시작
1) Properties Panel에서 Property 추가
2) Property type 선택 후 Name, Value (default value)로 세팅 후 Create

#### Text
3) (필요 시 Main Component 내 Properties Panel >> Multi-select option) Main Component의 Text 부분 (통일하게 묶고 싶은 Text) 선택 후 해당 **Text** Property 선택해 Layer에 연결 (layer 연결 아이콘 panel에서 선택)

#### Boolean
3) (필요 시 Main Component 내 Multi-select option) Main Component Show/Hide할 부분 (통일하게 묶고) 선택 후 **Appearance**에 있는 해당 Property에 대해 Layer 연결 옵션 선택

#### Icon/Instance Swap
3) (필요 시 Main Component 내 Multi-select option) Main Component의 icon 자체를 여러개로 swapping 하려면 **Icon section**에 있는 해당 Property에 대해 Layer 연결 옵션 선택
4) 필요 시 Preferred values (해당 Property에 즐겨찾기 옵션st) 설정 (아래 설명)
> **Tip:** Instance Swap Property 명칭을 설정할 때, Leading이면 (ㄴIcon OR ㄴLeading Icon) 등으로, Trailing이면 (Trailing Icon) 등으로 Rename

### Preferred values
: Instance swap 목록에 먼저 보여 줄 컴포넌트를 정하는 기능. 아이콘이 많아도 이 자리에 맞는 것만 골라 보여줌. (같은 자리에 항상 같은 icon등의 instance element를 적용할 때 **더 빠르게 설정 된 / 정해져 있는 아이콘 중에서만 선택**할 수 있게)
e.g., tab-bar에 항상 home, calendar, search, user 아이콘만 사용한다고 하면 tab-bar에 해당하는 Main Component의 아이콘은 preferred values로 해당 4가지 아이콘으로만 설정해서 tab-bar 수정할 때 4가지 중에서 빠르게 선택/수정 가능

**중요:** Property 이름은 잘 읽히는 통일 된 명칭으로 rename (e.g., Property1 대신 Label // Text 대신 Show icon // Swap 대신 Icon) [회사 renaming 내규에 따라서도 네이밍 방법 상이할 수 있음)


## Property 3종 (Property panel, Layer connection, Preferred values)

## Variant & Property
