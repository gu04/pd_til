# Week 3 (11/09 ~ 11/13)

## Prototype
: 화면을 실제 앱처럼 눌러보게 만든 시안. 개발 전에 흐름을 확인하고 팀과 같은 그림을 보기 위해 만듦

### Prototype의 목적
1) **검증 (Validation)**: 개발 전에 흐름 눌러서 문제 찾기 (e.g., (제품을 배포하기 전에 사용자가 겪는 문제를 파악하기 위한) 사용성 테스트 (UT))
2) **공유 (Sharing)**: PM/개발자/고객사, 모든 stakeholders가 같은 흐름을 봄
3) **설명 (Explanation)**: 움직임과 전환을 통해 말보다 직접 보여주기

## Prototype Tab & Flow

## 연결의 3요소
### Trigger/Action/Animation
   - Trigger (언제)
   - Action (어떤 행동을/무엇을)
   - Animation (어떤 비주얼 방식으로/어떻게)
   > e.g., brn/에약하기를 ```On tap 하면``` ```예약화면으로``` ```
### Trigger 종류
   - On tap/On click
   - On drag
   - While hovering
   - After delay (버튼이 아닌 *화면 프레임*에 걸기)
   - Key/Gamepad
### Action 종류
   - Navigate to
   - Back
   - Open overlay
   - Scroll to
   - Open link
> **주의:** Back action일 경우, Historical back을 사용 (Hierarchy back을 사용하려면 ```Navigate to action```을 이용)

## 연결도 (플로우 흐름도, 막힌 경로, 재생
: 화면 버튼으로 잇고, 돌아오는 길 (Back)과 자동 이동 (After delay)까지 연결
> **TIP:** 화면/페이지마다 들어가는 길, 나가는 길 둘 다 포함해야함
> **TIP:** 매 페이지마다 반복되는 Flow/Transition 화살표를 줄이고 싶다면 (e.g., Tab-bar) Main Component로 따로 설정 후에 반복 될 각 Transition을 Main Component에서만 정의 (화살표 잇기). Instance는 그대로 따라감. Alternatively, 각 버튼을 Main Component로 설정하고 Main Components 다 묶어서 Variant로 설정. 이후 Main Components 묶음 (Variant묶음) 각 페이지에 Instance로 붙여넣기.

막힌 경로 (Dead end)
: 다음 연결되는 페이지가 없거나, 백을 할 수가 없는 구조

> **TIP:** Preview에서 화면 내에 누를 수 있는/상호작용 할 수 있는 요소를 한번에 확인하려면 화면 밖 영역을 클릭하면 hover상태로 누를 수 있는 버튼 표시해줌
> **TIP:** Preview에서 ```Share Prototype``` 선택지


# 11/09/2026

## Variant 폭증
: 경우의 수마다 Variant를 만들면 Variant 개수가 곱셈으로 늘어남. 문구/아이콘까지 Variant로 만들면 관리하기 어려움. 그러나 개수가 많아지면 Component를 만드는 메인 이유 (수정을 쉽고 편리하게 하기 위한 shortcut)의 의미가 없어짐
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
: Instance swap 목록에 먼저 보여 줄 컴포넌트를 정하는 기능. 아이콘이 많아도 이 자리에 맞는 것만 골라 보여 줌. (같은 자리에 항상 같은 icon등의 instance element를 적용할 때 **더 빠르게 설정 된 / 정해져 있는 아이콘 중에서만 선택**할 수 있게)
e.g., tab-bar에 항상 home, calendar, search, user 아이콘만 사용한다고 하면 tab-bar에 해당하는 Main Component의 아이콘은 preferred values로 해당 4가지 아이콘으로만 설정해서 tab-bar 수정할 때 4가지 중에서 빠르게 선택/수정 가능

**중요:** Property 이름은 잘 읽히는 통일 된 명칭으로 rename (e.g., Property1 대신 Label // Text 대신 Show icon // Swap 대신 Icon) [회사 renaming 내규에 따라서도 네이밍 방법 상이할 수 있음)

## 라이브러리
(컴포넌트 모아서 다른 파일에서도 쓸 수 있게끔) 개발에서 모듈 import 같은 개념?

### 라이브러리 페이지
페이지 구조
: 컴포넌트와 스타일을 한 페이지에 모아 둔 것. **표지 (Cover)** 아래 **색/글자 기초 (Foundations)**와 **부품 (Components)**으로 나눔

1. Atomic Colour 정의 (원색표) -- 색 자체의 정의 (e.g., ```blue/500```)
2. Semantic Colour 정의 용도 이름 -- 정의한 Atomic Colour가 어디에 쓰는지의 정의 (e.g., ```text/primary```) 따라서, Semantic은 Atomic을 가리키는 구조
- Opacity는 icon/borderline등에 사용

**중요:**
- Cover, Foundation, Component, 그리고 Foundation 타입 (Colour, Typography 등) 등은 섹션 (Command+S) 별로 묶기
- 이름 슬래시로 종류 나누기
- 설명 Description을 1-2줄 쓰기 (DevMode에서 Component Information으로 쉽게 커뮨가능)

3. Primary, Label, Status, Line, Accent, Interaction, Status (의미론적 색상 (e.g. positive=green, cautionary=orange, destructive=red)), Inverse (다크모드일 때 쓰이는/위에 올라가는 색상들)

### Publish & Update

#### Publish
LHS bar에서 Asset (플러스 사인 로고) 선택  -> Libraries (책 모형) 선택 -> 발행을 원하는 모든 Elements, Components, Icons, Buttons 등을 가진 파일을 Publish
이 때 Published 파일의 요소들은 다른 파일에서도 사용할 수 있음

#### Update
새 파일 -> Assets -> Teams -> Add to file로 Published File의 요소들 새 파일로 import

**중요:** 기존 Published 파일에서도 내용을 바꿨다면 바꾼 부분 (Unpublished Changes)까지 다시 Publish하면 됨 (같은 방법으로)
**중요:** Draft에 있는 파일은 Publish 불가 (반드시 Team Project로 전환해야됨)

### 실무에서의 좋은 라이브러리 (체크리스트 & 디자인 시스템 첫 단계)

#### 체크리스트: 다른 사람이 처음 열어도 찾고, 고르고, 바로 쓸 수 있다면 좋은 라이브러리 ('필수는 아니지만 하면 좋은 것' 리스트)
1. 찾기
   - 섹션으로 나뉨
   - 기본 이름 없음
   - Description 있음
2. 고르기
   - Variant 이름 일관
   - Property 연결됨
   - Property Panel 만으로 변경 가능
3. 쓰기
   - Application Screen 1개 이상
   - Instance로만 조립
   - Detach 없음

**Key:** 하나의 큰 레고를 조립하듯이 블록블록 매칭할 수만 있게끔해야 usability maximised

#### 디자인시스템 첫 단계: 라이브러리는 디자인시스템의 첫 단계
1. 스타일 (색/스타일 등)
2. 컴포넌트 라이브러리 (Variant/Property)
3. 토큰/Variables (값이 이름 붙여 개발자가 쓸 수 있는 코드블럭/토큰)
4. 디자인 시스템 (규칙/문서/팀 운영)
