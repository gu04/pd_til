# Week 4
<img width="722" height="330" alt="image" src="https://github.com/user-attachments/assets/c21c4eec-739d-4d32-962e-ea7c45d81136" />

# 11/20/2026

## 1. 컴포넌트 기반 개발
## 컴포넌트란?
### HTML/CSS/JS
<img width="493" height="230" alt="Screenshot 2026-11-20 at 10 14 17" src="https://github.com/user-attachments/assets/a35f0e67-e295-4ee5-b95f-79b2228957ca" />

### 부품으로 조립 (Component)
**Component**: 화면을 이루는 **재사용 가능한 부품**. 요즘 웹/앱은 화면을 컴포넌트 단위로 만들어 조립함.
- Component 없이는 .html 화면/페이지마다 재사용되는 같은 요소도 각 화면/페이지별로 속성을 설정해야 함.
- Component는 각 재사용되는 요소별로 속성을 정의하는 부분 1개만 추가하면 됨.

## React
: 개발자들은 React를 써서 Component를 만듦. (웹 화면(UI)을 컴포넌트로 만드는 JS library) (메타가 만들었음)
- 컴포넌트(Component): 다시 쓰는 화면 조각
- 상태(State): 바뀔 수 있는 값 (사용자 행동에 맞춰 바뀌는 것)
- 렌더링(Rendering): 상태를 보고 화면을 그림 (값 -> 화면에 노출하는 것)

### 화면을 고치는 방식
: 예전에는 데이터가 바뀌면 화면을 직접 찾아 고쳤다면, React는 상태만 바꾸면 화면을 알아서 고침 (Main Component처럼)

### 컴포넌트 코드 (JSX)
: JS 안에 HTML처럼 쓰는 React 문법. 상태(JS)와 화면 모양(HTML)이 한 컴포넌트에 같이 있음.
> 각 컴포넌트 별로 속성/상태/렌더링 등을 정의하는 파일 (.jsx) -> 해당 .jsx 파일에 있는 요소들 속성 및 특징만 바꾸면 모든 화면/페이지 속성이 바뀔 수 있도록.

### Figma와 코드
: Figma 컴포넌트 속성과 코드 컴포넌트의 입력값은 거의 같은 모양.
<img width="493" height="126" alt="Screenshot 2026-11-20 at 10 29 07" src="https://github.com/user-attachments/assets/5ff7506d-63cc-4fd0-aad5-b4da7d885bee" />

## Props와 States
### Props
: 컴포넌트를 쓰는 쪽에서 넣어주는 값. 같은 Button에 다른 Props를 넣으면 다른 버튼이 됨.
<img width="502" height="156" alt="Screenshot 2026-11-20 at 10 35 02" src="https://github.com/user-attachments/assets/a1ebf825-017a-49b7-b0f5-e5214cbbfb77" />

### State
: 컴포넌트 안에서 사용자 행동에 따라 바뀌는 값.
#### Props vs. State
<img width="511" height="158" alt="image" src="https://github.com/user-attachments/assets/8a349bae-aec1-4fec-84ce-13455e719099" />
> **TIP:** Props는 밖에서 넣는 값, State는 안에서 바뀌는 값

## 컴포넌트 나누기
### 화면 쪼개기
: 반복되는 것부터 나눔. 여러 화면에서 다시 쓰이면 컴포넌트 후보.
<img width="571" height="203" alt="Screenshot 2026-11-20 at 10 37 39" src="https://github.com/user-attachments/assets/56c31a36-5282-4302-998b-157c4c592792" />
- 반복되는 요소를 .jsx로 만들어서 해당 파일을 반복해 넣고자 하는 화면의 .html파일 내로 import (`./jsx-file-name`)

### 이름 맞추기
: Figma와 코드의 컴포넌트/속성 이름이 같으면 질문이 줄어듦. (레이어, 컴포넌트, Variant 명칭 등)
<img width="571" height="167" alt="Screenshot 2026-11-20 at 10 39 43" src="https://github.com/user-attachments/assets/731f92f8-3fd4-4781-be53-befdbaa9dc94" />

## 2. Figma Dev Mode
## Dev Mode
### Design 모드 vs. Dev 모드
: 개발자가 디자인을 읽고 구현에 필요한 정보를 참고하는 Figma 화면 (Shift D 누르면 됨)
<img width="505" height="79" alt="Screenshot 2026-11-20 at 11 27 34" src="https://github.com/user-attachments/assets/fea84c78-1672-4ef8-8e61-a587a202623c" />

#### 디자인 모드와 비교
<img width="505" height="154" alt="Screenshot 2026-11-20 at 11 22 01" src="https://github.com/user-attachments/assets/79a1dac0-247b-4ae3-9cfc-80fb08d2776f" />

## 스펙 읽기
### Inspect 패널
: 크기, 간격, Auto Layout, 글자, 색, 변수, 컴포넌트 속성 등
- 레이어를 선택하면 오른쪽에 그 요소의 정보가 모두 보임

### 읽는 순서
: 개발자는 바깥 -> 안족, 배치 -> 모양 순서로 읽음.
<img width="505" height="181" alt="Screenshot 2026-11-20 at 11 29 07" src="https://github.com/user-attachments/assets/a01ec1b4-6261-4487-ba0c-5e9938b9a815" />

### 코드와 변수
: Code탭에서는 선택한 레이어의 CSS/iOS/Android 코드 조각을 자동으로 보여 줌으로서 그대로 쓰는 코드가 아니라 참고용으로만 쓰임.
<img width="501" height="132" alt="Screenshot 2026-11-20 at 11 31 38" src="https://github.com/user-attachments/assets/5c0575ac-e9be-47e4-a7b7-140134918778" />

### 에셋 내보내기
: 아이콘/이미지는 Inspect의 Assets에서 받음. 형식은 쓰임에 맞게
<img width="501" height="155" alt="Screenshot 2026-11-20 at 11 33 39" src="https://github.com/user-attachments/assets/a7463211-c6c7-4af4-91c2-c5ea3593398b" />
> **TIP:** 로고 같은 이미지의 경우, Position(상하좌우)을 Scale로 바꾸고 **Outline Stroke** 선택하기 (그래야 비율에 맞게 같이 커질 수 있음)

## 개발 준비 표시
### Ready for dev
: "이 디자인/프레임은 개발해도 돼요"의 표시. 개발자는 Dev Mode에서 표시된 것만 모아 봄. (각 프레임 우측 상단에 `</>` 표기를 누르면 됨 -> Dev Mode에서 Ready for development 패널(왼쪽)에 뜸)
<img width="708" height="274" alt="Screenshot 2026-11-20 at 11 34 20" src="https://github.com/user-attachments/assets/560cf993-eb00-45c5-8411-1c2f1a07cfcb" />
> **TIP:** 시안 여러 개 중 개발할 것만 Ready for dev로 표시하기!

### 주석과 측정 (Annotation)
: 화면에 안 보이는 규칙은 주석, 꼭 지켜야 할 간격은 측정으로 디자인 위에 직접 남김.
<img width="688" height="208" alt="image" src="https://github.com/user-attachments/assets/ebcd7eca-3625-4adb-bd76-bfbd52e07ff6" />

예시 1:
<img width="529" height="549" alt="image" src="https://github.com/user-attachments/assets/d2478b80-96d3-481b-b805-d9b6ff8aae7d" />

예시 2:
<img width="489" height="851" alt="image" src="https://github.com/user-attachments/assets/56b23544-9f35-4288-9699-ba78d1fa36f0" />

### 변경 확인
: Ready for dev 이후 고친 내용은 Dev Mode에서 이전 버전과 비교할 수 있음.
<img width="688" height="95" alt="Screenshot 2026-11-20 at 11 37 04" src="https://github.com/user-attachments/assets/c5ecc188-be54-4e62-a187-e0158cc540ec" />

## 3. 디자인 핸드오프와 협업 트렌드
### Handoff 과정
핸드오프: 디자인을 개발로 넘기는 것. 실무에서는 기획부터 QA까지 여러 번 나눠서 함께 함. (처음부터 끝까지 함께 하는 과정)
<img width="663" height="90" alt="Screenshot 2026-11-20 at 13 34 34" src="https://github.com/user-attachments/assets/228923fb-3892-4dd3-9d4f-8edb34b9818c" />
> **TIP:** 개발자한테서 자주 받는 질문은 미리 파일에 넣어두면 효율적으로 파일 주석/피드백을 주고 받을 수 있음
예시:
- 글자가 길면: 최대 길이/말줄임 규칙
- 로딩 중에는: 상태별 화면
- 다른 기기(e.g., 태블릿)에서는: 브레이크포인트별 화면
- 색이 변수가 있는지: 토큰/스타일
- 누르면 어디로 가는지: 화면 흐름/프로토타입
- 아이콘은 어디서 받는지: Export 설정 (Asset(아이콘, 이미지 등의 그래픽 요소)를 모아두는 프레임을 만들거나, 화면에서 직접 원하는 요소만 클릭해서 Export 가능하게끔)

## 핸드오프 패키지
### 체크리스트
: 개발자가 추가 질문 없이 볼 수 있게 8가지를 챙김.
<img width="577" height="221" alt="Screenshot 2026-11-20 at 14 10 12" src="https://github.com/user-attachments/assets/03138c4a-59f0-4e90-acc4-b709f5a9f850" />

### 파일 구조
: 화면의 흐름 순서대로 섹션을 나누고, 상태/예외는 따로 모아 둠. (개발자가 처음 열어도 어디부터 볼지 알 수 있게끔 정리)
<img width="561" height="285" alt="image" src="https://github.com/user-attachments/assets/063429c8-1ece-491f-885a-aa3d805fcbcd" />

### 디자인 QA
: 개발된 화면이 디자인대로 만들어졌는지 확인하는 단계
<img width="561" height="184" alt="Screenshot 2026-11-20 at 14 23 57" src="https://github.com/user-attachments/assets/0de858fb-32b5-49e5-9f12-f92b1b001dad" />

> **TIP:** QA 리스트 등은 PM이 제공함
> **TIP:** 개발자와 소통할 때는 디자인 요소들의 정확한 수치를 사용해서 설명하는 편이 훨씬 나음

## 협업 트렌드
### 디자인과 코드 잇기
: 디자인과 코드를 도구가 직접 잇는 방식 (아래 3가지 방법 등으로)
<img width="565" height="134" alt="Screenshot 2026-11-20 at 14 26 03" src="https://github.com/user-attachments/assets/edfb3aea-8469-44b1-a993-8ebdac72e5f9" />

### 디자이너의 역할
: AI도 사람도 파일의 구조를 읽음. 정리된 파일(레이어 이름이 직관적이게, 위치는 AL, 색값보다 변수를 사용)일수록 의도대로 만들어짐.
<img width="565" height="171" alt="image" src="https://github.com/user-attachments/assets/51d05654-975b-4226-86e6-a872f243a9a4" />

# 11/19/2026

## 1. HTML 구조와 시맨틱 태그
## 웹 화면의 재료
### 웹의 3대 언어
- HTML: 구조 (뼈대)
  - 웹 페이지의 뼈대와 구조, 제목, 문단, 이미지, 링크 등 기본 내용 정의.
- CSS: 디자인 (스타일)
  - 웹 페이지의 디자인, 스타일, 색상, 글꼴, 레이아웃, 여백 (시각적 꾸미기)
- JS: 기능 (동작하는 것)
  - 웹 페이지의 동적인 기능, 상호작용 (사용자의 행동에 반응하는 이벤트 처리, 애니메이션, 데이터 처리 등)<img 

### 디자인과 코드
피그마랑 웹 개발 사이 연결 포인트
<img width="673" height="204" alt="Screenshot 2026-11-19 at 10 20 00" src="https://github.com/user-attachments/assets/8ef8988c-5213-4c38-8132-a87b16812df1" />

## HTML의 기본

### 태그 (HTML Tag)
<img width="673" height="204" alt="image" src="https://github.com/user-attachments/assets/e2d24b9a-c75a-48f2-82be-25659b50a83c" />

### 자주 쓰는 태그
<img width="673" height="289" alt="image" src="https://github.com/user-attachments/assets/630604e5-6992-4022-9d43-bc6c5de67d34" />

## 시맨틱 태그
: 생김새가 아닌, 의미를 나타내는 태그 (보여지는 화면은 똑같아도 보조 기술이 읽는 내용이 달라짐)
### `<div>`만 쓴 화면 (Semantic HTML)
: 어떤 부분이 어떤 이름으로 묶이는지 알기 어려움. 접근성 부분이 저해될 수 있음.
<img width="673" height="236" alt="Screenshot 2026-11-19 at 10 38 32" src="https://github.com/user-attachments/assets/8d5bb64d-3624-4a6a-b521-9ca0a1452500" />
예시:
<img width="673" height="324" alt="image" src="https://github.com/user-attachments/assets/384d3830-01d7-4e14-a6dc-7861ac605dae" />

> **TIP:** Figma 레이어도 영역 이름으로 묶어둬야 같은 구조 그대로 HTML로 반영하기 좋음.

## 2. CSS 박스 모델 & Flexbox

## CSS 기본
CSS: 어떤 요소를 무엇을 어떻게 바꿀지 적는 규칙
### 규칙 구조
<img width="489" height="151" alt="Screenshot 2026-11-19 at 11 20 55" src="https://github.com/user-attachments/assets/b0cc858a-40bb-4ee5-9c50-1b0c3749175a" />
- 앞에 . 찍는게 Class (`.class-name`): class-name에 해당하는 모든 요소를 그룹핑해 한번에 속성 바꾸기
- 앞에 # 쓰는건 Id (`#id-name`): 단일 id-name 요소만 속성 바꾸기

### 속성 대응
<img width="489" height="211" alt="image" src="https://github.com/user-attachments/assets/824ba656-2d6d-4f54-9876-01f39eb59d52" />

## 박스 모델
### 4겹의 상자
내용 -> 안쪽 여백 -> 테두리 -> 바깥 여백 순서
<img width="489" height="190" alt="image" src="https://github.com/user-attachments/assets/e0fb0300-5e2a-4856-b2d2-518ec87b4ff3" />
> **TIP:** 버튼 크기는 1)글자, 2)패딩, 3)테두리 로 결정
> **TIP:** Padding 값등의 박스 모델 dimension은 시계방향으로 적기 (위, 오, 아래, 왼 순으로)

### Figma와 비교
<img width="670" height="201" alt="Screenshot 2026-11-19 at 11 33 05" src="https://github.com/user-attachments/assets/fb68cd17-c2d5-49a5-8340-515b7f187d24" />
> **TIP:** 개발자들은 요소 간 Auto Layout에서 자동정렬(Horizontal/Vertical AL)의 거리는 Gap이라고 하지만 Frame-단위(첫번째 선택지) 거리는 margin을 사용해서 설정

## Flexbox (Flex <=> Auto Layout)
: 요소를 가로/세로로 나란히 놓고 간격/정렬을 정하는 CSS방식 (AL이랑 같은 개념이라 1:1로 대응됨)
> AL을 쓰는 부분이라면 Class/id 속성 안에 `display: flex;` 로 시작함
### Auto Layout 대응
<img width="674" height="279" alt="image" src="https://github.com/user-attachments/assets/2afe90d6-f13e-4cdd-8329-23d0ab6b5cff" />

## 3. JavaScript & 상태(State)
: 사용자 행동을 감지 후 값을 바꾸고, 바뀐 값에 맞게 화면을 다시 그림.

## 이벤트와 상태
### 이벤트 (Event/동작 흐름):
1. 사용자 행동 (e.g., 찜 버튼 탭)
2. 이벤트 감지 (e.g., click)
3. 상태 변경 (e.g., liked: false -> true)
4. 화면 변경 (e.g., 하트 채움 / 찜 수 +1)

### 상태 (State)
: 지금 화면이 어떤 모습인지 정하는 값. 값이 바뀌면 화면도 바뀜
예: `liked = false` // `liked = true`
 **TIP:** Code에서의 State는 Figma에서의 Variant 같은 것

## 화면 상태
: 데이터를 불러오는 화면은 최소 **4가지** 모습을 가짐
- 로딩 (Loading)
- 빈 화면 (Empty State): 서비스의 목적을 위한 주 사용자 행동을 유도함
- 오류 (Error): 휴리스틱9에 따라 오류의 원인과 해결책 제공
- 정상 (Default)
<img width="586" height="282" alt="image" src="https://github.com/user-attachments/assets/40e9ca0b-8380-4819-bcc3-7652c3e1f38d" />

## 버튼 상태 (Button State)
<img width="594" height="211" alt="image" src="https://github.com/user-attachments/assets/bb9a749a-3af1-4c80-8704-7a0fad02039c" />

## 구현 제약
실제 데이터: 길고, 비어 있고, 느릴 수 있음.
- 긴 글자 (예: 클래스 이름이 40자라면?)
- 빈 데이터 (예: 후기가 0개라면?)
- 느린 응답 (예: 3초 넘게 걸린다면? -> 스켈레톤 활용하기, 효율적인 로딩을 위해 겹치는 요소 제외하기)
- 다른 화면 (예: 태블릿에서 연다면?)

# 11/18/2026

## 1. 웹 접근성
: 모든 사용자(장애인/고령자/다양한 기기가 환경을 쓰는)가 웹/앱의 정보와 기능을 제약없이 인식/탐색/이용할 수 있도록 보장하는 것.

### 영구/일시/상황
- **영구적**
  : 시각/청각/운동 장애 등
- **일시적**
  : 다치거나 수술한 뒤 잠깐
- **상황적**
  : 환경 때문에 생기는 제약 (e.g., 한 손으로만 스마트폰을 봐야 하는 상황에서 생기는 불편함/문제 등도 포함!)

### 보조 기술 (Assistive Technology)
: 사용자가 기술을 사용할 수 있도록 돕는 기술.
- 스크린리더: 화면 글자/버튼을 소리로 읽어줌 (VoiceOver/TalkBack)
  > 이미지 대체 텍스트 설정하기, 아이콘 버튼 라벨 활용하기
- 화면 확대/큰 글씨: 글자와 화면을 크게
  > 글자 200%에도 화면에서 잘리지 않게
- 키보드/스위치: 손 대신 키로 이동/선택
  > 포커스 순서와 표시 (**TIP:** 그래서 웹 상에서는 FOCUS 상태(state)를 포함하고 있는게 중요함 / 직접 터치가 어렵거나 시각적으로 보이지 않아 locate하기 어려운 경우 `tab` 만으로 버튼 선택 등이 가능하게끔)
- 색 보정/고대비: 색을 바꾸거나 대비를 높임
  > 색에만 의존하지 않기 (색맹/색약을 가지고 있는 사용자 접근성을 위해)

## WCAG 2.1
: W3C가 만든 **웹 콘텐츠 접근성 지침**. 모든 4가지 원칙 아래에 있음.

### 4대 원칙
1. Perceivable (인식의 용이성): 볼 수 있거나 들을 수 있게
2. Operable (운둉의 용이성): 누르고 이동할 수 있게
3. Understandable (이해의 용이성): 읽고 쉽게 이해할 수 있게
4. Robust (견고성): 보조 기술과 맞게 동작하게

### 등급 (A/AA/AAA)
: 기준마다 등급이 있음. 대부분의 기관/서비스는 **AA**를 목표로 함.
- A: 최소 기준. 못 지키면 쓸 수 없는 사람이 생김 (e.g., 이미지 대체 텍스트, 색에만 의존 금지)
- **AA**: 대부분의 법/기관이 목표로 하는 기준 (e.g., 명도 대비 4.5:1, 포커스 표시)
- AAA: 가장 엄격한 기준 (e.g., 명도 대비 7:1)
> **TIP:** 'Color Generator' plug-in 같은 경우, 각 컬러별 등급마다 & 컬러마다 위에 대비를 맞추기 위한 추천 색상이 뜸
> **TIP:** 피그마 내 각 요소별로 색상 내부 탭(맨 오른쪽 세그먼트 - "Check color contrast")으로 가독성을 위한 대비감 평가가 가능함.

## 접근성을 위한 디자이너의 기준

### 명도 대비
: _본문 글자_ 는 **4.5:1**, _큰 글자_(24px 이상/굴기 19px 이상)와 UI 요소 테두리는 **3:1** 이상이어야 함.
<img width="639" height="181" alt="image" src="https://github.com/user-attachments/assets/4d34b261-2ab5-4e7e-9305-e747f9bbf901" />

### 색 외 단서
: 색으로만 정보를 전달하진 않음 (색맹/색약 등의 사용자를 고려해서). 오류/선택/상태는 **아이콘/글자와 함께** 씀.
예시:
<img width="637" height="310" alt="image" src="https://github.com/user-attachments/assets/db40b1c0-960a-40bd-879b-1a933f3e4782" />

### 터치/포커스/확대
: 잘 누를 수 있고, 키보드로 보이고, 크게 설정해도 깨지지 않아야 함.
<img width="637" height="182" alt="image" src="https://github.com/user-attachments/assets/baeefca8-ae94-4985-b83c-c8c45479d667" />

<img width="637" height="316" alt="image" src="https://github.com/user-attachments/assets/09a4169c-7f40-4223-89a4-191f0a6db04a" />

### 대체 텍스트 (Non-text Content)
: 이미지/아이콘 버튼 대신 읽어 줄 수 있는 글. 디자이너가 화면 의도를 알기 때문에 핸드오프에 함께 적음.
예시:
<img width="637" height="186" alt="image" src="https://github.com/user-attachments/assets/41564c63-7044-4bcd-9572-e48481fecf03" />

## 2. 접근성 점검 연습
## 측정 도구
### 대비 재기
: 글자색 배경색 HEX를 도구에 넣으면 대비율이 나옴. 눈대중이 아니라 숫자로 판정함.
1. 색 2개 고르기 (글자색 & 배경색의 HEX)
2. 도구에 넣기 (WebAIM Contrast Checker/Figma 플러그인 등)
3. 비율 읽기
4. 기준과 비교
> **TIP:** 가장 밝은 부분과 대비가 낮을 때 (배경이 하얀색이면 글자가 밝으면 가독성 떨어지는 등) Overlay, Dimmer 등의 사용.

### 판정 읽기
: 요소마다 어떤 기준(본문/큰 글자/UI)을 적용할지 먼저 정하고 판정함.
<img width="646" height="208" alt="Screenshot 2026-11-18 at 10 49 49" src="https://github.com/user-attachments/assets/a0819361-4c21-41de-b020-8807c25ae3b3" />

## 점검표
### 점검 항목 6가지
: 점검할 수 있는 질문/방법
<img width="646" height="223" alt="image" src="https://github.com/user-attachments/assets/768179ca-e5a1-4820-954b-bddf17bfba7b" />

## 수정 우선 순위
1. 막히는 것 (Critical): 사용자가 서비스를 이용할 때의 주 목적 달성이 어려울 때
   > e.g., 라벨 없는 버튼, 대비 낮은 버튼
2. 자주 보는 것: 모든 화면에서 불편할 때
   > e.g., 본문 회색, 작은 터치 영역
3. 나머지: 불편하지만 진행은 됨
   > 장식 이미지 대체 텍스트, 보조 정보 대비

## 3. 디자인시스템 사례 분석
## 왜 디자인 시스템이 필요한지
- 시스템이 없을 때: 화면마다 조금씩 다른 버튼이 생기고, 사용자도, 팀도 일관되지 않은 소통방식으로 인해 헷갈릴 수 있음
### 디자인 시스템
: 서비스를 만드는 원칙/스타일/컴포넌트/사용 규칙을 한곳에 모은 것
  1. 일관성: 사용자가 덜 헷갈림
  2. 속도/효율성: 같은 걸 다시 만들지 않음
  3. 협업: 디자이너/개발자/AI가 같은 이름을 씀 (Agile Environment 팀 내 통일된 언어)

## 구성 요소
### 4가지 구성
: 원칙 -> 파운데이션 -> 컴포넌트 -> 가이드
1. 원칙: 무엇을 중요하게 여기나 (Brand values?)
2. 파운데이션: 색/글자/간격/아이콘
3. 컴포넌트: 버튼/입력칸/카드
4. 가이드: 언제/어떻게 쓰나

### 디자인 토큰 (Design Token)
**아토믹 -> 시맨틱 구조를 색/글자/간격 전체**로 넓혀 **팀 규칙**으로 정한 것. 디자인(Figma 변수)과 코드가 같은 이름으로 사용.
<img width="651" height="254" alt="Screenshot 2026-11-18 at 13 23 54" src="https://github.com/user-attachments/assets/ef4b87c5-43ba-4a07-a98f-c6a7ae91eea4" />

## 사례 비교
### 공개 디자인시스템
: 많은 회사/기관이 디자인시스템을 공개함. 읽기만 해도 실무 기준을 배울 수 있음.
<img width="659" height="150" alt="image" src="https://github.com/user-attachments/assets/99c6f1c8-6dc3-4061-908b-9c6011cdc0ad" />

### 버튼 가이드
: 같은 버튼도 디자인시스템마다 가이드가 다름. 총 5가지 항목으로 나뉨.
<img width="659" height="218" alt="image" src="https://github.com/user-attachments/assets/d377fa61-2f78-4faf-a1b4-7c220f0866c4" />


# 11/17/2026

## 1. 그리드 시스템과 4/8배수 간격
## 그리드
: 화면이 정돈되어 보이도록 설정하는 것

### 컬럼/거터/마진
: 어떤 디바이스에서든 같은 비율로 변환해 요소들을 일관되게 배치할 수 있게끔 돕는 가이드라인
- 컬럼: 내용이 놓이는 세로 칸
- 거터: 컬럼 사이 간격
- 마진은 화면 양끝 여백
> **TIP:** 정보량이 많은 시스템은 컬럼이 좁고 트렌디한 미니멀한? 시스템은 비교적 넓음

## 4/8배수 간격
### 왜 4/8 배수?
: 왜냐면 **디자인 값 X 기기 배율 = 실제 픽셀**이라, 어느 배율에서도 딱 떨어짐
<img width="1333" height="555" alt="image" src="https://github.com/user-attachments/assets/ef635e25-b308-4d19-a3cd-9d5c51ca727a" />
> Figma에서 작업했을 때 360의 배수의 px로 설정되는거라서 360, 720, 1080, 1440 등으로 픽셀이 더 촘촘해지니까 픽셀로 나누면 4,8의 배수 요소 사이즈여야 정수로 떨어짐
> 정수가 아닌 소수로 떨어지면 픽셀이 뭉개져 보이는 현상 발생할 수 있음
<img width="1333" height="555" alt="Screenshot 2026-11-17 at 10 16 25" src="https://github.com/user-attachments/assets/175fe7ce-5953-45ea-b015-77ebcdb9943b" />
> **TIP:** 원래는 8의 배수를 쓰는게 정석이지만 디자인에 따라 8배수는 요소 사이 간격이 멀어질 수도 있으니까 더 작은 4의 배수도 괜찮음

### 스페이싱 스케일 (Spacing Scale)
: 쓸 간격 값을 미리 정해 둔 목록. 타입 스케일처럼 이 안에서만 고름.
<img width="1333" height="387" alt="image" src="https://github.com/user-attachments/assets/277f17f0-8d50-4bcd-94ea-15954ed99bfa" />
> **TIP:** 시간적 리소스가 있고 디자인 시스템이 잘 구축되어 있는 곳들은 Spacing도 값을 미리 저장할 수 있음 (0, 100, 200등의 이름으로)

### 간격(Gap) 정하는 순서
: 안쪽부터 바깥쪽으로, 가까운 것은 좁게, 다른 묶음은 넓게
무슨 요소들의 사이인지에 따라 Spacing이 달라짐
<img width="1333" height="477" alt="Screenshot 2026-11-17 at 10 24 27" src="https://github.com/user-attachments/assets/e3fe994e-fa6b-409a-b763-a7884ead422a" />
> **TIP:** 디자인/브랜드 이미지에 맞춰서 Spacing이 기본적으로 넓어지거나 좁아질 수는 있으나 한 시스템 내 여백 패턴은 그대로 유지해야됨.

## Auto Layout과 연결
### Auto Layout 간격:
: Figma Auto Layout의 Gap(간격)과 Padding(안쪽 여백)에 스케일 값을 넣음. 개발 코드에도 같은 값이 그대로 쓰임.
<img width="673" height="191" alt="Screenshot 2026-11-17 at 10 27 42" src="https://github.com/user-attachments/assets/2204f650-2513-4709-88e3-6746186c84cb" />
> 개발자에게 핸드오프할 때는 dev mode에서 규격이 padding, margin 등이 px로 나타날 수 있게 Auto Layout 사용
> **TIP:** 보통 마진은 16이나 20정도 (에어비앤비는 24)

## 2. 스크린 사이즈 & 브레이크포인트
### 단위
- px(픽셀): 화면의 점. CSS px는 **기기 배율을 반영한** 논리 단위 {웹(CSS)/이미지파일}
- pt(포인트): **기기 배율과 상관없는** 논리 단위 (포인트) {iOS}
- dp(디피): 160dpi 화면을 기준으로 한 논리 단위 {Android}
> **TIP:** 이미지는 픽셀을 사용하되 배율 별로(**3배수** 이상) 내보내기

#### 배율
: 같은 크기에서 더 많은 픽셀을 그리는 정도. 요즘 폰은 대부분 @2x 혹은 @3x 화면 (해상도 높게)
e.g, iOS에서의 24pt 아이콘을 배율로 그린다면:
- @1x: 24 x 24 px
- @2x: 48 x 48 px
- @3x: 72 x 72 px
> 아이폰은 SVG 형식으로 씀 (벡터) -- 이미지는 Export에서 x3배수 정도의 SVG로 내보내기

### 브레이크 포인트
: 레이아웃이 바뀌는 **화면 폭** 기준. 기기 이름이 아니라 **폭(가로) 구간으로 정함**.
<img width="496" height="145" alt="image" src="https://github.com/user-attachments/assets/67d39f0b-ba62-495a-9fb5-6e6617a99926" />

### 레이아웃 변화
#### 바뀌는 패텬
: 화면이 넓어질 때 자주 쓰는 4가지 변화. 하나 이상을 섞어 씀.
<img width="695" height="236" alt="image" src="https://github.com/user-attachments/assets/04aaf981-fed3-4d2e-bec8-a6700b4f47f1" />

#### 한 화면, 3 크기
: 폭에 따라 바뀌는 모습
<img width="695" height="287" alt="image" src="https://github.com/user-attachments/assets/965cf1fe-c237-4d0a-be30-b64d442081c8" />

## 3. iOS와 Android
### 같은 기능, 다른 규칙
- iOS: Apple HIG Design System (Guide)
- Android: Material Design System (Guide)

차이점:
<img width="499" height="164" alt="image" src="https://github.com/user-attachments/assets/48c1c8d0-85f3-43fc-83eb-b3892c63c25c" />
> iOS는 뒤로가기 버튼이 default로 없으니까 화면 안 왼쪽 위의 뒤로가기 버튼이 중요함 -> 뒤로가기 버튼에 라벨을 달기 때문에 화살표 꼬리를 달지 않는 경우가 많음. 페이지 메인 이름은 그래서 중간에 두는 경우가 많음.

### 안전 영역 (Safe Area)
: 상태바/다이내믹 아일랜드/홈 인디케이터에 가려지지 않는 영역. 버튼과 중요한 내용은 이 안에 둠.
> 배경 색깔 등은 Safe Area 밖으로 가도 됨

#### 시스템 영역
: 앱이 그리지 않는데 화면을 차지하는 영역. 디자인할 때 함께 그려 두고 확인함.
- 상태바: 시간/배터리/알림
- 키보드: 입력하면 화면 절반을 가림
- 제스처 영역: 홈 인디케이터/뒤로가기 스와이프

### 웹 (에서만 있는 요소 상태 (state))
: 마우스와 키보드로 쓰는 웹에는 모바일에 없는 상태가 있음. 버튼 하나에 상태 5가지를 그려 둚.
- 호버(Hover)
- 포커스(Focus)
(기본(Default), 누르는 중(Pressed), 누를 수 없음(Disabled) 상태들은 웹&모바일 둘 다 유지)
> OS(Operating System/체제) 규칙(뒤로 가기/Safe Area)과 웹의 호버/포커스를 생각하기

# 11/16/2026

## 1. 색채 이론과 UI 컬러
## 색의 3속성
: 색상 | 채도 | 명도 (Figma의 HSB 색 선택기랑 같은 구조)
- **색상 (Hue)**: 색의 **종류** (빨강/파랑) - 브랜드를 대표하는 색
- **채도 (Saturation)**: 색이 얼마나 **선명한지** - 채도가 높을수록 시선 집중
- **명도 (Brightness)**: 색이 얼마나 **밝은지** - 글자와 배경의 대비를 정해줌
> UI에서는 명도가 가장 중요함 (요소의 위계를 명도로)
> **주의:** 채도는 많이 쓰지 않도록 (시선이 너무 많이 분산되지 않게)

### 대비율
: 대비가 낮으면 글자가 안 읽히고 중요한 버튼도 묻힘. 밝기 차이를 대비율로 재는 것.
> **TIP:** 정해져 있는 대비율 기준을 참고하면 됨

## 역할별 컬러
: 색은 이름(e.g., blue) 대신 역할(e.g., primary)로 정함. 왜냐면 색을 바꿔도 화면을 균형감 있게 특정 역할에 쓰이는 색이 달라도 전체적인 다른 역할 색들의 조합이 쉬움.
- Primary: 브랜드/가장 중요한 행동
- Secondary: 보조 강조 (선택 사항)
- Neutral: 글자/배경/구분선
- Status: 성공/경고/오류/정보 등

### 컬러별 의미
: 색마다 사용자가 먼저 떠올리는 신호가 있음. 그 신호와 맞는 자리에 써야 헷갈리지 않음.
- 빨강: 긴급/오류/할인
- 파랑: 신뢰/안정/확인
- 초록: 성공/완료/건강
- 노랑: 주목/주의/공지
- 보라: 특별함/프리미엄
- 검정: 고급스러움/집중

### 상태 컬러
: Semantic Colour 중 성공/경고/오류처럼 상태를 알리는 색. 역할과 다른 의도로 쓰이면 사용자에게 혼란을 줄 수 있음. 
- 성공: 초록
- 경고: 주황
- 오류: 빨강
- 정보: 파랑
> **TIP:** 브랜드 컬러 자체가 상태 컬러와 비슷하다면 해당 상태에 해당할 색상을 브랜드 색상과는 차이를 두도록 (채도를 바꾼다던지 등)

### 컬러 조함
- 보색: 강렬함/주목
> **주의:** 자주 쓰면 눈이 피곤함
- 유사색: 안정감/편안함
> **주의:** 자주 쓰면 지루함/지겨움

## 60-30-10 비율
: 60% 기본색 // 30% 보조색 // 10% 강조색 (강조가 적을수록 눈에 띔)

## 디자인 토큰

### 컬러 스케일 (Colour Scale)
: 색 하나를 밝기 단계 (50-900)로 나누고, 배경/테두리/글자에 맞는 단계를 골라씀
- 각 색상 마다 밝기를 밝음-어두움 10단계로 나누는 것

### 컬러 토큰 구조 (Design Token)
: 색/간격 같은 값이 붙인 이름 (디자인 토큰). 실무에서는 색 값 -> 아토믹 -> 시맨틱 순서로 이름을 쌓아 씀.
원시 값 (색 그 자체) -> 아토믹 토큰 (색 이름을 붙인 이름) -> 시맨틱 토큰 (어디에 쓰는지에 붙는 이름) -> 컴포넌트 토큰 (특정 부품 전용 (보통 대규모 프로젝트에서만 사용))
> 화면에서는 역할 대신 색의 Design Token (e.g., blue/500)을 쓰기

### 디자인 토큰 파일 (Design Token File)
: 디자인 토큰을 개발자도 읽을 수 있게 정리한 파일(주로 JSON). Figma 변수 -> 토큰 파일 -> 코드 순서.
프로세스
1. Figma 변수
2. 토큰 파일 (JSON)
3. CSS 변수 {개발자가 고치고 확인}
4. 실제 화면 구축/코딩

### 원시 값 -> 아토믹 토큰 -> 시맨틱 토큰
: 원시 값 (e.g., #0057FF) -> 아토믹 토큰 (blue/500)으로 base color 업데이트 -> 

### 시맨틱 이름 짓기
: 요소/의도/강조/(상태)를 이어 붙여 만듦.
<img width="897" height="312" alt="image" src="https://github.com/user-attachments/assets/52c017bd-beba-4423-ab07-c6139c60e951" />

## 라이트/다크 모드

### 로컬 베리어블 (Local Variable)
: 파일 안에서 만든 변수 목록. 컬렉션 -> 모드 -> 변수 3단으로 정리

### 모드 나누기

### 모드별 연결

### 라이트 & 다크 차이
: 색을 뒤집는 게 X. 배경/글자/브랜드 색/깊이를 따로 조정하는 것
다크의 경우
- 배경: 순검정 대신 짙은 회색
- 글자: 순백 대신 조금 낮춘 흰색
- 브랜드 색: 한 단계 밝고 덜 진하게
- 깊이: 그림자 대신 밝기로 (왜냐면 다크모드에서는 검은 그림자등을 표현 못하니까 배경 자체를 더 연하게 하는 등)

### 라이트/다크 계층
예: 같은 이름의 값만 바뀜. 라이트는 그림자 크기로, 다크는 면의 밝기로 층을 나눔.

## 2. 타이포그래피 계층
## 글자의 계층
### 계층이 없는 화면
: 글자가 모두 같은 크기/굵기면 뭐부터 읽어야 할지 알 수가 없음.

### 텍스트 계층
: 글자를 역할별 단계로 나누고, 단계마다 크기/굵기/행간을 하나로 정해둠
- Display (e.g., 32/Bold/130%) {가장 큰 제목}
- Title {섹션별 제목}
- Heading 1 (e.g., 24/Bold/135%) {소제목}
- Heading 2 (e.g., 20/Bold/140%)
- Body (e.g., 16/Regular/150%) {본문}
- Caption (e.g., 13/Regular/140%) {작은 보조 정보들}

## 타입 스케일
### 타입 스케일 (a.k.a. Font Size)
> **주의:** 타입 스케일에서는 4,8배수 규칙 적용 X (4/8배수 규칙은 Spacing에서만 해당)
> **TIP:** [모바일]에서는 타이포그래피를 **Regular보다 굵게**, **크기는 12-13pt 보다는 크게**

### 행간 (Line Height)
: 줄과 줄 사이 간격
> **주의:** 행간 = 100%라면 각 줄 사이 간격이 0이라서 가독성이 떨어질 수 있음

### 자간 (Letter Spacing)
: 글자와 글자 사이 간격. 한글 본문은 기본 자간(0) 혹은 아주 미세한 -0.01em/-0.02em이 가장 
> **TIP:** 보통 자간은 -0.01em / -0.02em 정도인데 피그마에는 em 단위가 없어서 주로 -1%~-2%로 둠 (대신 -2% 이하로는 떨어지지 않게)

### 한글 서체 고르기
: UI 서체는 모양보다 잘 읽히는지, 굵기가 추운한지, 써도 되는지를 먼저 봄
서체 고르는 기준
1. 가독성
2. 굵기 단계
3. 라이선스 (상업적으로 써도 되는지)

#### Serif(명조) vs. San Serif(고딕)
<img width="892" height="445" alt="image" src="https://github.com/user-attachments/assets/fa6a27a8-7f99-4e6d-a0fd-65439b47588c" />
> **TIP:** 인간과 친화적이려는 목적이면 명조 // 정보 전달이 우선이면 고딕 (그래서 AI 플랫폼(e.g., Perplexity, 기존의 Claude)이 주로 인간에게 잘 다가가도록 명조를 자주 쓴다는 연구 결과가 있음)

## 텍스트 스타일
### 스타일(Text Style)로 정리
: 계층을 Figma 텍스트 스타일로 등록하면 값이 아니라 이름을 씀 (개발자도 같은 이름으로 받음)
프로세스
1. 계층 정하기 (Display/Heading/Body/Caption 등)
2. 값 정하기 (크기/굵기/행간 등)
3. 스타일 등록 (설정한 스타일 이름 붙이기 e.g., `heading/24-bold`)

## 3. 아이콘 시스템
## 아이콘 스타일
### 라인 & 면
- **라인** 아이콘: 가볍고 깔끔함. **기본 상태**에 많이 씀.
- **면** 아이콘: 눈에 잘 띔. **선택된 상태**에 쓰기도 함. 대신 면 아이콘을 기본 아이콘으로 사용할 때는 _명도를 높이기_.

### 섞인 아이콘
: 스타일/크기/선 두께가 섞이면 같은 역할의 아이콘도 다른 것처럼 보이고 상태가 불분명해 보임.

## 크기 & 터치 영역
### 크기 단계
: 아이콘도 **4의 배수** 스케일로 많이 씀 (기본은 24, 작게는 16/20, 크게는 32)
- 16 (목록 옆 작은 표시)
- 20 (버튼 안 아이콘)
- 24 (기본/탭/헤더)
- 32 (빈 화면/강조)

### 터치 영역 (Touch Target)
: 아이콘이 24여도 누르는 영역은 손가락 크기만큼 넓게.
> **TIP:** 터치 영역 권장: **iOS는 44 x 44** pt, **Android는 48 x 48 dp** 이상
> **주의:** 통상 아이콘 크기를 Touch Target 크기에 꽉 채워 맞추는 게 아니라 아이콘을 24 x 24, 터치 영역을 48 x 48 OR 44 x 44 등
> 

## 라벨과 라이선스
### 라벨과 함께 쓰기
: 뜻이 명확한 아이콘(홈/검색/닫기)이 아니라면 글자 라벨을 함꼐 씀.
(예: 하트 아이콘은 '찜'의 의미인지, '좋아요'의 의미인지 헷갈릴 수 있음.
> **TIP:** `React Icons for Figma` 등의 Figma Plug-ins 자유롭게 쓸 수 있음

## 4. 정보 위계 설계
## 시선의 흐름
### 시선 흐름 패턴
: 사람은 화면을 처음부터 끝까지 읽지 않고 훑어봄.
- 글이 많은 화면은 F형태로 (중요한 말은 줄 앞에)
- 단순한 화면은 Z형태로 훑음 (행동 버튼은 끝 지점에)
<img width="643" height="294" alt="Screenshot 2026-11-16 at 14 55 49" src="https://github.com/user-attachments/assets/4494faa7-68c4-4ad6-a39c-4296c4d98998" />

### 화면의 주인공
: 화면에서 가장 먼저 봐야 할 정보 하나를 정하고, 나머지는 그 뒤로 보냄.

## 위계를 만드는 도구 (How to form Hierarchy)
: 위계는 크기/대비/여백/위치를 조합해서 구성
- **크기**: **클수록** 먼저 봄
- **대비**: **굵기/색** 차이가 클수록 눈에 띔
- **여백**: **가까우면** 묶이고 멀면 나뉨
- **위치**: **위/왼쪽**을 먼저 봄

### 여백의 역할 (White Space)
: 여백은 남는 공간이 아니라 정보를 묶고 나누는 도구. 덩어리 사이를 넓히면 순서가 보임.

## 위계 개선
: 크기/대비/여백/위치를 조정해서 목적에 맞는 위계를 명확하게.

### 위계 점검 질문
1. 3초 안에 주요 정보가 보이나?
2. 흐리게 봐도 순서가 남나?
3. 강조색은 몇 곳인가? (1-2곳 강조된거면 OK, 그 이상이면 줄이고 없으면 추가하기)
4. 같은 역할은 같은 스타일인가?
