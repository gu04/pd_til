# Product Design TIL

## 11/04/2026

### 1. Responsive Layout (반응형 레이아웃)

#### 1.1 Fill Container & Auto Layout

Parent Frame 크기에 따라 Child Frame도 함께 늘어나도록 설정하는 방법

- **Width: Fill** → Parent의 너비 변화에 맞춰 좌우로 늘어남.
- **Height: Fill** → Parent의 높이 변화에 맞춰 위아래로 늘어남.
- **Fill Container 조건:** Child의 직속 Parent에 Auto Layout(AL)이 적용되어 있어야 함.
- 중첩된 Child까지 반응형으로 만들려면 각 단계의 Parent에 AL을 적용하고, 필요한 Child도 AL로 두어 Width/Height를 Fill로 설정.

#### 1.2 Auto Layout vs. Constraints

| 구분 | Auto Layout (AL) | Constraints |
|---|---|---|
| **용도** | 콘텐츠 배치 및 크기 자동 조정 | Parent 크기 변화에 따른 위치·크기 유지 |
| **주요 설정** | Fill, Hug, Gap, Auto Spacing | Left, Right, Top, Bottom, Scale |
| **적용 예시** | 카드, 버튼 그룹, 콘텐츠 영역 | Status Bar, Indicator, Navigation Bar 등 고정 배치 요소 |

**핵심 원칙**
- **위치가 고정**되어야 하는 요소: 필요에 따라 AL 대신 Constraints 사용.
- **고정은 아니지만 유동적인** 콘텐츠: AL + Child Fill + Auto Spacing 사용
- **좌우 여백**을 유지하며 늘어나는 요소: Constraints → `Left + Right` (w/o AL)
- **위아래 여백**을 유지하며 늘어나는 요소: Constraints → `Top + Bottom` (w/o AL)

---

### 2. Navigation & Tab Bar

#### 2.1 Top Bar (상단 탑바)

**주요 유형**
1. **Home Header:** 홈 화면 상단 헤더.
2. **Back Navigation Bar:** 상세 페이지 등에서 이전 화면으로 돌아가는 탑바.
3. **Search Top Bar:** 검색 기능 중심의 탑바.

##### Back Navigation Bar 구조

| 영역 | 역할 | 예시 |
|---|---|---|
| **Leading** | 왼쪽 버튼 영역 | 뒤로가기 |
| **Title** | 현재 페이지 제목 | 상품 상세 |
| **Trailing** | 오른쪽 버튼 영역 | 좋아요, 장바구니, 더보기 |

- Leading / Trailing 버튼은 **Icon + Auto Layout**으로 터치 영역(Touch Target)을 설정.
- 버튼 내부와 버튼 그룹에 각각 AL을 적용하는 중첩 구조(AL × 2) 활용 가능. (항상 Icon위에 AL을 씌워야 Touch target 조정 가능한 Button 생성 가능)

##### Hierarchy Back vs. History Back

- **Hierarchy Back:** 상위 → 하위로 이동한 화면 계층을 역순으로 돌아감.
- **History Back:** 실제 방문한 페이지 기록을 역순으로 돌아감.

**UX Tip:** History Back은 방문 경로가 길어질 수 있으므로, Home으로 바로 이동하는 옵션을 추가하면 편리함.

#### 2.2 Bottom Tab Bar (하단 탭바)

앱의 주요 화면 사이를 이동하는 내비게이션.

##### Selection State (선택 상태)

| 방식 | 특징 |
|---|---|
| 상태 구분 없음 | 모든 탭이 회색 → 현재 위치 파악 어려움 |
| 색상만 변경 | 색각 이상 사용자에게 접근성이 낮을 수 있음 |
| **색 + Bold Text + Filled Icon** | 여러 시각적 단서로 선택 상태를 명확하게 전달 (권장) |

- 선택된 아이콘을 채울 때는 아이콘 내부의 **Fill × Fill (Width × Height)** 설정 확인 (버튼 사이 갭 없이 상하좌우 다 Fill the bar)
- **탭 간 Gap:** `0`으로 설정해 터치 영역이 서로 인접하도록 구성.
- **Touch Target:** 수업 기준 40~44px 정도 확보.
- **탭 개수:** 일반적으로 3~5개 권장.

##### Hick's Law (힉의 법칙)
: 선택지가 많아질수록 사용자의 의사결정 시간이 로그 함수적으로 증가하는 경향이 있음
(User's **decision-making time increases logarithmically with the number of choices** provided)

- 하단 탭 개수를 제한해 탐색 부담을 줄임.
- 탭이 너무 많으면 정보 구조를 재정리하는 것이 좋음.

#### 2.3 Segment Tab (세그먼트 탭)
: **한 화면** 내에서 콘텐츠의 카테고리나 표시 영역을 전환하는 탭

- Bottom Tab과 달리 앱의 최상위 화면 이동보다는 **현재 화면 내** 콘텐츠 전환에 사용.
- 선택한 항목 아래에 Underline Indicator 표시.
- Indicator는 별도 선보다 **Bottom Stroke**로 구현하는 방법 권장.
  - Dev Mode에서 Border 속성을 확인하기 쉬움.

---

### 3. Card Component (카드)

#### 3.1 Card Types

| 유형 | 구조 |
|---|---|
| **Stacked Card / Vertical Card** | 이미지와 정보를 세로로 배치 |
| **Card / Normal** | 일반적인 카드 레이아웃 |
| **Card / List** | 이미지와 정보를 가로로 배치 |

#### 3.2 Card Anatomy (카드 구성 요소)

카드에 포함될 수 있는 요소들 (Optional):

1. **Thumbnail (썸네일)**
   - 대표 이미지 또는 배경 이미지
   - Chip / Badge 등 추가 정보 표시 가능

2. **Information (정보)**
   - 제목
   - 메타데이터 (날짜, 위치 등)
   - 가격
   - 남은 자리 / 재고

3. **CTA (Call-to-Action)**
   - 사용자에게 다음 행동을 유도하는 버튼 또는 선택지 (e.g., 예약하기, 자세히 보기)

#### 3.3 Lock Aspect Ratio (이미지 비율 고정)

- 카드 크기가 변해도 이미지의 가로·세로 비율을 유지하는 기능.
- Figma의 크기 설정에서 **Lock Aspect Ratio** 활용.
- 반응형 카드에서 이미지/썸네일이 찌그러지지 않도록 설정.

#### 3.4 Truncate Text (긴 제목 처리)
: 긴 제목이 카드 레이아웃을 깨뜨리지 않도록 제한

**권장 설정**
- 제목 최대 **2줄** 표시.
- 초과하는 텍스트는 `...`으로 생략.
- Typography 설정에서:
  1. `Truncate Text` 활성화.
  2. `Max Lines = 2` 설정.
  3. 텍스트 Width → `Fill Container`.

**중요:** Truncate가 정상적으로 작동하려면 텍스트 영역의 너비가 제한되어야 함. AL 내부의 반응형 카드에서는 **Width: Fill**로 설정.

---

### 4. Calendar Component (캘린더)

#### 4.1 Calendar Layout

**7열 그리드(7-Column Grid)** 구조로 구성.

1. 날짜 셀 한 개 당 **34x34 AL** 1차 씌우고 하단에 **dot 4x4** AL (세로) → AL 전체 **44x48 Fixed**
2. 날짜 셀 7개 Duplicate + 가로로 AL 배치 → **Week Frame** 생성.
3. Week Frame들을 세로로 쌓아 → **Month Frame** 생성.
4. 각 날짜 셀의 Width → `Fill Container`.
5. 각 Week / Month Frame에 필요한 AL 적용.

#### 4.2 Date Cell States (날짜 셀 상태)

| State | 시각적 표현 | 의미 |
|---|---|---|
| **Default** | 기본 텍스트 | 일반 날짜 |
| **Today** | Outline / Border | 오늘 날짜 |
| **Selected** | Filled Background | 사용자가 선택한 날짜 |
| **Disabled** | Gray Text | 선택할 수 없는 지난 날짜 |
| **Available** | 숫자 아래 Dot | 예약 또는 선택 가능한 날짜 |

**UX 원칙**
- 날짜별 상태가 시각적으로 명확하게 구분되어야 함.
- Today와 Selected는 서로 다른 스타일로 구분.
- Disabled 날짜는 선택 불가능하다는 사실을 명확히 전달.
- Dot Indicator를 활용해 선택 가능한 날짜를 빠르게 파악하도록 설계.

---

### 5. Key Takeaways

- **Responsive Layout:** Child의 AL Width/Height Fill (w/ auto spacing) + 직속 Parent의 AL
- **Auto Layout:** 유동적인 콘텐츠 배치와 크기 조정에 활용
- **Constraints:** Parent 크기 변화에도 특정 위치·여백을 유지해야 하는 요소에 활용 (e.g., status_bar, indicator, tab-bar)
- **Top Bar:** Leading / Title / Trailing 구조와 Back Navigation 방식 구분
- **Bottom Tab Bar:** 3~5개 탭, 충분한 Touch Target, 명확한 Selection State
- **Segment Tab:** 동일 화면 내 콘텐츠 전환 + Underline Indicator.
- **Card:** Thumbnail + Information + CTA, 이미지 비율 고정 및 텍스트 Truncate.
- **Calendar:** 7열 Grid + Fill Container + 날짜별 시각적 State.

## 11/03/2026

### 1. Figma Layout & Constraints

#### 1.1 Constraints vs. Fill Container

| 기능 | 발동 조건 | 설명 |
|---|---|---|
| **Constraints** | Parent가 Frame일 때 | Parent의 크기가 변경될 때 Child의 위치 및 크기를 어떻게 유지할지 설정 |
| **Fill Container** | Parent에 Auto Layout이 적용되어 있을 때 | Child가 Parent의 사용 가능한 공간에 맞춰 크기를 조정 |

#### 1.2 Hug / Fill / Fixed

Child Frame 기준으로 이해하기:

- **Hug Contents:** 자신의 내부 콘텐츠 크기에 맞춰 Parent Frame 크기가 조정됨.
- **Fill Container:** Child가 Parent의 사용 가능한 공간에 맞춰짐. (Parent의 Auto Layout 필요)
- **Fixed:** Parent나 내부 콘텐츠 크기에 관계없이 지정된 크기를 유지함.

**Note:** Hug은 콘텐츠에 맞춰 자신의 크기를 조정하는 설정이며, Fill은 부모 Auto Layout의 사용 가능한 공간을 채우는 설정이다.



#### 1.3 Auto Layout & Position

- Auto Layout이 적용된 Parent 내부에서는 Child의 위치가 자동으로 관리됨.
- Child를 드래그해 자유롭게 이동하려고 하면 Auto Layout의 배치 규칙에 따라 원래 위치로 돌아갈 수 있음.
- **Ignore Auto Layout:** Child를 Auto Layout의 배치 흐름에서 제외하고 자유롭게 배치할 수 있도록 하는 기능.
- Ignore Auto Layout을 사용하지 않고 위치를 조정하려면 Parent의 Padding, Gap, Alignment 등을 변경해야 함.

---

### 2. Mental Model (멘탈 모델)

사용자가 인터페이스와 상호작용할 때 머릿속에 형성하는 **작동 방식에 대한 이해와 기대**.

- 사용자가 인터페이스를 어떻게 사용할 것이라고 생각하는지
- 특정 요소를 보고 어떤 동작을 예상하는지
- 기존 경험을 바탕으로 어떤 결과를 기대하는지

---

### 3. Button

#### 3.1 Button States (버튼 상태)
: 사용자의 현재 상호작용 상태를 알려주고, 다음 액션을 이해할 수 있도록 시각적 피드백을 제공하는 것.

일반적으로 동일한 Atomic Color 계열 내에서 명도(Brightness)를 조절해 States를 구분함.

| State | 설명 |
|---|---|
| **Default** | 기본 상태 |
| **Hover** | 마우스 커서를 올렸을 때 (일반적인 모바일 터치 UI에는 적용되지 않음) |
| **Pressed** | 버튼을 누르고 있는 상태 |
| **Focus** | Tab 키 등으로 요소가 선택된 상태. Outline 등으로 표시 |
| **Disabled** | 비활성화 상태. 클릭하거나 조작할 수 없음 |

#### 3.2 Button Hierarchy (버튼 위계)
: 버튼의 중요도와 역할에 따른 분류

| Hierarchy | 역할 |
|---|---|
| **Primary** | 화면에서 가장 중요한 핵심 액션 |
| **Secondary** | Primary를 보조하는 액션 |
| **Tertiary** | 상대적으로 중요도가 낮은 부가 액션 |
| **Assistive** | 사용자의 작업을 돕는 보조 기능 |
| **Destructive** | 위험하거나 되돌리기 어려운 액션 (e.g., 예약 취소, 회원 탈퇴) |

#### 3.3 Button Style

- **Solid (Filled / Contained):** 배경색이 채워진 버튼
- **Outlined:** 테두리(Stroke) 중심의 버튼
- **Text (Ghost):** 배경이나 테두리 없이 텍스트 중심으로 구성된 버튼

#### 3.4 Button Colour

- 버튼의 Fill 색상은 가급적 Opacity를 변경하지 않고, 지정된 Color Token을 사용.
- 상태별 차이는 동일한 Atomic Color 계열 내에서 Brightness를 조절해 표현.
- 단순 배경 위에 텍스트를 배치하는 경우에는 Opacity를 조절하는 사례도 많음.

#### 3.5 Button Size

- **S (Small)**
- **M (Medium)**
- **L (Large)**

크기 조절 방법:
1. 버튼 Height를 Fixed 값으로 지정.
2. 버튼의 Font Size와 Padding 등을 조절.

Layer에서 버튼 명칭: ```btn/hierarchy/size/state```

#### 3.6 Touch Target (터치 영역)

- 버튼의 터치 영역(Touch Target)은 수업 기준 **최소 40 × 40px**로 디자인.
- 주변 UI 요소들로 인해 버튼 자체의 시각적 크기를 키우기 어려운 경우, **실제 버튼 크기는 유지하면서 터치 영역만 확장**할 수 있음.
- 통상 회사에서 지정한 Design Guide에 명시 (그걸 따르면 됨)

**Figma 적용 방법:**
1. 버튼을 감싸는 터치 영역용 Frame 생성.
2. `Ignore Auto Layout`을 활용해 기존 레이아웃에 영향을 주지 않도록 설정.
3. 터치 영역을 최소 40 × 40px로 확장.
4. 버튼의 시각적 크기와 위치는 그대로 유지.

**Note:** Visual Size(시각적 크기)와 Touch Target(실제 터치 가능 영역)은 다를 수 있음. Figma에서 터치 영역을 확장했다면 실제 개발에서도 동일하게 적용해야 함.

### 4. Badge
: 아이콘이나 카드 옆에 배치되는 작은 UI 요소로, 숫자·상태·새로운 소식 등을 한눈에 전달함.

#### 4.1 Badge Types

| Type | 설명 | 예시 |
|---|---|---|
| **Count** | 숫자 표시 | 누적 알림 개수 |
| **Label** | 텍스트 및 색상으로 상태 표시 | 긴급, 정보, 주의, 성공 |
| **Dot** | 작은 점으로 새로운 상태 표시 | 읽지 않은 알림, 새로운 소식 |

#### 4.2 Badge Colour

- **Red:** 긴급, 위험
- **Blue:** 정보, 일반 상태
- **Yellow:** 주의, 경고
- **Green:** 성공, 완료

### 5. Input Field

#### 5.1 Input Field States

| State | 시각적 특징 | 구성 요소 |
|---|---|---|
| **Empty (Blurred)** | 입력값이 없는 기본 상태 | Gray Placeholder + Helper Text |
| **Focus** | 입력 필드가 활성화된 상태 | Blue Stroke/Border & Icon + Cursor + Input Text + Helper Text |
| **Filled** | 사용자가 값을 입력한 상태 | 진한 색상의 Input Text + Helper Text |
| **Error** | 입력 오류가 발생한 상태 | Red Stroke/Border + Error Message + Warning Icon (!) |
| **Disabled** | 입력이 불가능한 상태 | Gray 스타일 + 필요시 Helper Text |

#### 5.2 Input Field Elements

- **Placeholder:** 입력 전 표시되는 예시 또는 안내 텍스트. 일반적으로 Gray 색상.
- **Input Value:** 사용자가 실제 입력한 값. Placeholder보다 진한 텍스트 색상.
- **Helper Text:** 입력 방법이나 조건을 안내하는 보조 텍스트.
- **Error Message:** 어떤 오류가 발생했는지 구체적으로 설명하는 텍스트.
- **Warning Icon:** 오류 또는 주의가 필요한 상태를 시각적으로 전달하는 아이콘.
- **Cursor (Caret):** 입력 위치를 나타내는 커서.

Error 상태에서는 단순히 빨간색으로 표시하는 것보다, **정확히 어떤 오류인지 설명하는 Error Message**가 중요함.

#### 5.3 Input Field Uses

**ID / Username**
- 사용자 아이디 입력

**Password**
- 비밀번호 입력
- Show / Hide Password Toggle 옵션 제공 가능

**Search**
- 검색어 입력
- Clear (X) 버튼을 통해 입력한 검색어 전체 삭제 가능

**Note:** 이때, Keyboard 올라오게 하려면 기존 Community 디자인 활용 가능 (버튼 Keyboard 바로 위에 위치 재설정 가능)

### 7. Key Takeaways
- **Constraints:** Parent Frame을 기준으로 Child의 위치와 크기 반응을 설정.
- **Fill Container:** Auto Layout이 적용된 Parent의 사용 가능한 공간에 맞춰 Child 크기를 조절.
- **Hug / Fill / Fixed:** 콘텐츠에 맞춤 / 부모 공간에 맞춤 / 지정된 크기 유지.
- **Ignore Auto Layout:** Auto Layout의 배치 흐름에서 제외하고 자유롭게 위치를 지정.
- **Component States:** 사용자의 상호작용 상태를 시각적으로 전달.
- **Button Hierarchy:** 액션의 중요도와 역할에 따라 구분.
- **Touch Target:** 버튼의 시각적 크기와 실제 터치 가능 영역을 구분하여 설계.
- **Badge:** 숫자, 라벨, 점을 활용해 정보를 빠르게 전달.
- **Input Field:** 입력 상태에 따라 시각적 피드백을 제공하고, 오류 발생 시 구체적인 안내가 중요.

## 11/02/2026
### Figma Auto Layout & GUI vs. Product Designer

#### 1. Figma Auto Layout 기본

##### 간격(Spacing)
- 모든 간격값은 **4의 배수**로 설정 (4, 8, 12, 16 …)
- 일관된 리듬 // 개발 핸드오프 시 수치가 깔끔해짐

##### Wrapping 옵션
- Auto Layout의 **Wrap** 옵션을 켜면 가로 공간이 부족할 때 자식 요소가 다음 줄로 넘어감
- 태그, 칩, 카드 그리드처럼 개수가 가변적인 요소에 유용

##### Overflow (스크롤)
- 방향: **Horizontal** / **Vertical**
- 작동 조건: **부모 프레임이 자식(콘텐츠)보다 작아야 함**
  - 부모 프레임 ≥ 자식 프레임 → 넘칠 내용이 없어서 스크롤 작동 X
  - 부모 프레임 < 자식 프레임 → 넘친 영역이 스크롤됨

##### Ignore Auto Layout (Absolute Position)
- 자식 요소 **위에 겹쳐 올리는 요소**(배지, 플로팅 버튼 등)는 해당 요소에 **Ignore auto layout** 적용
- Auto Layout에서 빠져 자유롭게 위치 지정 가능
- 화면 상단/하단에 고정해야 한다면 Ignore 후 **Top / Bottom constraints** 설정

##### Fill Container로 하단 고정
- `content` 프레임의 **높이(H)**를 **Fill container**로 설정
- `content`가 남는 높이를 모두 차지하므로 `tab-bar`가 자동으로 맨 아래로 밀려남

---

#### 2. 레이어 구조 예시 (Home 화면)

```
home
├── status-bar
├── content                (H: Fill container)
│   ├── section/greeting
│   ├── section/search
│   └── section/section-title
├── tab-bar                (options/navigations)
└── indicator
```

- 레이어 이름은 역할 기준으로 명확하게 (`section/…` 처럼 슬래시로 그룹핑)
- 구조가 명확해야 Auto Layout 동작과 개발 핸드오프가 수월함

---

#### 3. GUI Designer vs. Product Designer

| 구분 | GUI Designer | Product Designer (PD) |
|---|---|---|
| 중점 | 시각적 요소(Visual) | 문제 정의 → 해결 → 검증의 전 과정 |
| 문제 정의 | 사용자 경험 중심 | 사용자 경험 + **비즈니스 임팩트** 기준 |
| 비즈니스 연결 | 원래의 비즈니스 목표까지 거슬러 연결할 필요는 적음 | 회사가 달성하려는 목표와 직접 연결해야 함 |
| 협업 범위 | 주로 디자인 영역 | PM, SWE, DA, DS 등 전 직군과 협업 |

##### Product Designer의 업무 프로세스 (PDVC Iteration)
1. **문제 정의 (Problem Definition)**
   - 가설 수립 → 실제 사용자 인터뷰로 검증 → 문제 정의 수정
   - 일상에서 사람들이 겪지만 흔히 간과되는 문제를 발견하는 것이 핵심
2. **디자인 (Design)**
3. **검증 (Validation)**
   - 사용성 테스트(Usability testing) 등
4. **협업 (Collaboration)**
   - PM, SWE, DA, DS 등과 함께 진행

##### 필요 역량
- **Business Acumen**: 비즈니스가 어떻게 돌아가는지, 회사가 무엇을 달성하려는지에 대한 감각
- 사용자의 일상 속 Needs/Pain Points를 파악하는 관찰력
- 가설 검증을 비즈니스 임팩트 관점에서 판단하는 능력
- **판단 (judgment) 능력**: AI가 출력하는 output에 대해 그대로 적용할지, 첨삭할지에 대해 판단할 줄 알아야됨

##### 예시: 토스's 조직 구조
- 제품 영역별(카드, 증권, 송금, 페이 등)로 한 팀을 구성
- 각 팀에 **PM, PD, SWE, DA** 등이 모두 포함되어 해당 영역을 end-to-end로 담당
