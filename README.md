# Product Design TIL

## 11/03/2026
###
Constraints 발동 조건: Parent가 frame 이어야 됨
Fiil 발동 조건: Parent가 Autolayout 이어야 됨
State: 사용자의 다음 액션을 알게 함 -- atomic colour 계열 내에서 명도/brightnes만 바꿈
* Default
* Hover (모바일 적용 X)
* Pressed
* Focus (Tab 눌렀을 때 선택됨 -- outlined button)
* Disabled (누를 수 X)
Mental Model (멘탈모델): interface와 상호작용할 때 거치는 생각 (사용하는 방법)
Button Hierarchy (버튼 위계)
* Primary
* Secondary
* Tertiary
* Assistive
* Destructive (위험 요소 e.g., 예약 취소, 탈퇴)
Button Style
* Solid (Filled, Contained)
* Outlined
* Text (Ghost)
Button Colour (버튼 fill은 opacity 바꾸지 X, 대신 그냥 배경에 텍스트 올릴 때는 opacity altering 하는 경우 다수)
Button Size (height값을 fixed두기 OR 버튼 글자 크기 조정)
* S
* M
* L

Badge: 아이콘/카드 옆에 있는 작은 표시/숫자/상태/새 소식을 한눈에
* 숫자 (count (e.g., 누적 알림 개수))
* 라벨 (급한 상황: RED, 정보/나머지: BLUE, 주의: YELLOW, 성공: GREEN, etc.)
* 점 (e.g., 알림이 있을 때/새 소식이 있을 때)
Child 입장에서 Hug/Fill/Fixed:
* Hug: 자신에 Parent가 맞춤 (금쪽이를 품어줌)
* Fill: 자신이 Parent에 맞춤 (Parent 항상 autolayout on)
* Fixed: 자신의 사이즈는 Parent, 자기자신에 상관 X

Input field states
* Empty (Blurred) -- placeholder (gray text as example) + helper-text (instructions on what to input)
* Focus -- stroke/border & icon blue (cursor bar) + value/input text + helper-text (instructions on what to input)
* Filled -- placeholder와는 다르게 진한 text colour that the user filled in + helper-text (instructions on what to input)
* Error -- stroke/border red + error text (정확히 어떤 error 인지/error message의 중요성) + ! 사인 (주의 심볼) + helper-text (instructions on what to input)
* Disabled -- 입력 불가 상태 (all gray as example) + helper-text (instructions on what to input)

Input uses
* 아이디
* 비밀번호 (show password toggle 옵션도 있음)
* 검색 (검색어 모두 지우기 X 옵션 있음)

버튼 반경 원래는 40px 기준으로 디자인 되어야 되는데 다른 요소들에 둘러쌓여서 쉽게 사이즈를 크게 바꾸지 못 하는 경우 -> ignore auto layout 후 터치 반경만 높이기


# Figma & UI Design Notes

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

##### 예시: 토스's 조직 구조
- 제품 영역별(카드, 증권, 송금, 페이 등)로 한 팀을 구성
- 각 팀에 **PM, PD, SWE, DA** 등이 모두 포함되어 해당 영역을 end-to-end로 담당
