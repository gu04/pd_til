# Week 5

# 11/26/2026

##  1. UX/UI / 코드 / 마인드셋

## UX/UI 법칙
### 휴리스틱/UX 법칙
(단순히 "불편해요"보다 객관적으로 어느 원칙이 깨졌는지 특정 **기준에 대한 진단**으로 바꾸기)

### 색 / 타이포 / 정보 위계
(**크기/대비/여백/위치**로 뭘 먼저 보게 할지 정하기)
> **TIP:** 사용자가 우선순위로 삼아야 할 요소를 파악하고 위계를 설계할 수 있음

### 그리드 / 디바이스
(같은 화면도 크기마다 열과 규칙이 달라짐)
<img width="600" height="270" alt="Screenshot 2026-11-26 at 10 13 03" src="https://github.com/user-attachments/assets/17c1e966-36ad-4f44-acdf-14352470c3cf" />
> Break Point (기기마다 달라지는 레이아웃 기준), Margin (요소 밖을 둘러싸는 spacing), Grid (기준 선을 지켜 열과 규칙을 정확하게 설정)

### 접근성 / 디자인 시스템
(원칙 -> 파운데이션 -> 컴포넌트 -> 가이드 로 일관되게끔)
<img width="600" height="232" alt="Screenshot 2026-11-26 at 10 14 52" src="https://github.com/user-attachments/assets/b0a22f01-27e1-4fec-b5b0-8d60a5003c8c" />

### HTML/CSS/JavaScript
- Figma의 AL <=> CSS의 Flexbox (flex-direction은 정렬 (row/column)
- HTML은 뼈대, CSS는 스타일, JavaScript는 행동/상호작용

### 컴포넌트 개발 / 핸드오프
(Figma 속성(Variant/Text/Boolean)이 코드의 Props가 됨)
<img width="574" height="148" alt="Screenshot 2026-11-26 at 10 23 06" src="https://github.com/user-attachments/assets/b94fe34a-aa1f-4100-a3fa-3dd3bc5f1955" />

### 헷갈리는 원칙 짝 정리표
<img width="703" height="244" alt="image" src="https://github.com/user-attachments/assets/6c51e8c4-0558-4e23-85f9-ce70d6d50679" />

> **TIP:** 일관성과 표준성의 휴리스틱에 어긋나면 Learning Curve가 높아짐 (사용자가 새로 받아들이고 배워야 할 인터페이스 패턴이 많음)

### 문제 진단 문장 3요소
<img width="703" height="151" alt="Screenshot 2026-11-26 at 10 28 09" src="https://github.com/user-attachments/assets/09210e77-3331-47f4-93a8-c8eac86d58a9" />

## HTML
### HTML 핵심 요소, 태그
- `<!DOCTYPE html>`
- `<html lang="ko"></html>`: 언어를 한국어로 설정함. 브라우저 내에서 설정된 언어로 쓰이면 해당 언어를 쓰는 사용자들의 검색 결과 등에 더 잘 뜰 수 있음
- `<head></head>`: 브라우저에서 프로세싱 되는 메인 정보
- `<meta>`
- `<title></title>`: 탭의 이름/제목
- `<body></body>`: 브라우저 내 본문 내용

> **TIP:** `index.html` 파일에서 느낌표(!) 치고 Tab(->|)을 누르면 자동으로 placeholder 뼈대 만들어줌

### 자주 쓰는 태그
<img width="706" height="272" alt="image" src="https://github.com/user-attachments/assets/95738424-8a14-4f4d-9f17-84b4da8a982f" />

#### Text Size (글자 크기)
<img width="213" height="340" alt="Screenshot 2026-11-26 at 11 22 26" src="https://github.com/user-attachments/assets/60b262fa-1154-427c-baed-8302b1713c20" />

### HTML 포맷
<img width="659" height="127" alt="image" src="https://github.com/user-attachments/assets/0f320e16-1b80-4377-ad00-980a50d894d5" />

## CSS
### HTML에 CSS 연결
- <link rel="stylesheet" href="style.css"> 로 묶기 (rel은 어떤 스타일 문서로 관계 정의할지, href는 repository내 어떤 파일/문서에 해당 스타일을 연결할건지 (디폴트는 style.css 파일))
> **TIP:** CSS는 <head></head> 사이에 붙여넣기

### CSS 포맷
<img width="351" height="84" alt="image" src="https://github.com/user-attachments/assets/cc71ef2d-3578-418a-a6bf-872cba4e7a4f" />

> **주의:** CSS는 각 스타일 끝에 semi-colon(;) 추가해야됨!!!

### 선택자 3가지 종류 (tag, class, id)
- Tag (HTML의 여러 태그 (종류) e.g., p{} // img{} // h3{})
- Class (class="type" 안의 type에 해당하는 모든 요소들에 해당)
- Id (id="element"안의 element에 해당하는 element 요소 하나에 해당)

> **TIP:** 보통 **ID는 JS로 요소 하나를 찾을 때** 주로 쓰는데, 나머지 **실무 상황에서는 Class**를 사용.

### Class vs. ID
- `.class`
  : 여러 요소의 스타일을 한 번에 바꿀 때 유용 (class 이름 placeholder에 같은 요소들의 공통된 이름으로 대체)
- `#id`
  : 단 하나의 요소의 스타일을 바꿀 때 사용 (id 이름 placeholder에 해당 요소 이름으로 대체)

### Figma 속성 <=> CSS 속성
<img width="645" height="216" alt="Screenshot 2026-11-26 at 13 31 42" src="https://github.com/user-attachments/assets/4048de3f-991a-4ce8-b160-d5ab2add8234" />

### Box Model (박스 모델)
: 모든 요소는 내용 -> 안쪽 여백 -> 테두리 -> 바깥 여백 순서 (안 -> 밖 순)
<img width="645" height="145" alt="Screenshot 2026-11-26 at 13 33 02" src="https://github.com/user-attachments/assets/4d68f988-e1c2-4ca2-b38c-0130c45e9480" />

### Flex = AL
: `display: flex`라면 AL처럼 방향/간격/정렬을 따로 정할 수 있음
<img width="645" height="238" alt="Screenshot 2026-11-26 at 13 33 45" src="https://github.com/user-attachments/assets/4bc1c9e8-52f0-4e52-b9f9-11219a280ded" />

## JavaScript
(Figma Prototype의 트랜지션과 같은 흐름)
### JS가 하는 일 3단계
1. 찾기: 화면에서 버튼/숫자를 찾음
   - **`querySelector`** 함수로 찾음
2. 기다리기: 버튼 클릭 등의 사용자&요소 간의 상호작용 기다림
3. 바꾸기: 글자/모양/숫자 등을 바꾸기

### HTML, CSS, JS 주석(Comment)
HTML | CSS | JS
----|----|----|
`<!--comment-->` | `/* comment */` | `// comment`

## AI 도구 / Junior Designer 마인드셋


# 11/25/2026

## 1. Figma/프롬프트 복습

## Product Designer 직무
### GUI -> PD
(화면 표현 -> 사용 흐름 -> 문제와 결과)
<img width="421" height="293" alt="image" src="https://github.com/user-attachments/assets/8e81783c-d4e2-49c7-b4bd-b3a30b3a3f1d" />

## PD 채용공고
: 공고 문장은 1) 문제정의, 2) 설계, 3) 검증, 4) 협업 으로 나눠 읽음
<img width="570" height="229" alt="Screenshot 2026-11-25 at 10 16 42" src="https://github.com/user-attachments/assets/5fc19e28-1502-4b20-8d94-c3f5f17309a6" />

## AI 시대 PD의 역할
AI라는 새 도구를 사용하지만 판단하는 일은 사람이 함.
<img width="570" height="280" alt="Screenshot 2026-11-25 at 10 18 06" src="https://github.com/user-attachments/assets/3e1b2695-ab90-4bb5-be21-8d9a6bd160ee" />

## AI Literacy
### AI가 답을 만드는 방법
: 다음에 올 말을 확률로 골라 이어 붙임. LLM은 Next-Token Prediction으로 다음 토큰을 확률로 전환해 최대한 그럴듯/자연스럽게 답을 생성
> **주의:** Hallucination이 생길 수 있음 (AI는 맞히면 보상을 주기 때문에 보상을 받기 위해 찍어가며 맞힐 수 있음)

### 프롬프트 구성요소
1) 역할 (<persona>)
2) 맥락 (<context>)
3) 과업 (<task>)
4) 형식 (<format>)
5) 제약 (<constraints>)
6) 예시 (<example>) - **Few-shot**

### AI의 한계와 답변 검증 절차
1. 쪼개기: 숫자/날짜/이름/인용이 들어간 문장을 하나씩 떼기
2. 1차 출처 (Primary source): 내용을 처음 발표한 곳에서 직접 확인
3. 판정, 확인일: 맞음/틀림/확인 불가로 적고, 확인한 날짜를 남기기

### 책임 있는 AI 활용
: 내보내기 전에 출처, 권리, 사용 사실을 확인
1) 출처 확인
2) 권리 확인
3) 사용 사실 밝히기

### 동료 테스트 (The Colleague Test)
: 보내기 전, 상황을 모르는 동료가 읽어도 이해할 수 있는지 확인하는 방법 (Anthropic Prompt Guide에서)
// 동료가 헷갈리면 AI도 헷갈릴 확률 높음

### v0 -> v3 개선 (Version Control)
: 한 번에 한 칸씩 더하면 무엇이 결과를 바꿨는지 보임.
<img width="714" height="215" alt="image" src="https://github.com/user-attachments/assets/d19c2a60-3036-45b2-a3d8-6510a2da6f2b" />

## Figma 마스터
<img width="550" height="267" alt="Screenshot 2026-11-25 at 11 20 14" src="https://github.com/user-attachments/assets/d5f1aeca-18bb-4bdb-92c8-be0b20645e01" />

### Variant & Property
<img width="550" height="222" alt="image" src="https://github.com/user-attachments/assets/5eea604f-ae3a-4de0-9c01-2512f9239d1f" />

- Variant: 모양 (e.g., 상태 State, 크기 Size, 종류 Type)
- Property: 내용 (e.g., 글자 Text, 보이기 Boolean, 인스턴스 Instance Swap)

> **TIP:** `spacer` 등을 rectangle로 만들어서 왼 요소가 숨겨져도 (Boolean False 되어도) 오 정렬인 요소는 위치 그대로로 둘 수 있음.

### UI 컴포넌트
#### 헷갈리는 짝 (생김새보다 "누르면 어떤 액션이 일어나는가"로 구분하기)
<img width="706" height="222" alt="Screenshot 2026-11-25 at 14 21 25" src="https://github.com/user-attachments/assets/c45f6e39-1145-473b-b450-84806d317a97" />

# 11/24/2026

## 1. 디자인 맥락 프롬프트

## 맥락 없는 요청
> AI는 우리의 서비스, 사용자, 그 화면에서 무슨 일이 있었는지 모름

### 6가지 구성요소
1. **역할** (AI가 맡을 입장)
2. **맥락** (서비스/사용자/상황 정보)
3. **과업** (AI가 정확히 해야 할 일)
4. **형식** (결과물의 모양)
5. **제약** (지켜야 할 조건)
6. **예시** (원하는 결과의 샘플)

## 백락 블록
### 맥락 블록 3가지
: AI는 우리 서비스를 모르기 때문에, 디자이너가 아는 맥락을 3칸으로 나눠 넣음
1. 서비스
   : 무슨 서비스, 어떤 말투
2. 사용자
   : 누가, 어떤 상황에서
3. 화면 상황
   : 어느 화면, 직전에 무슨 일을 하는지

### 맥락 블록 예시 (클로드 .xml 포맷)
```
<context>
  <service> 모임핏: 동네 운동 클래스 예약 앱. 친근하지만 가볍지 않은 해요체. </service>
  <user> 퇴근길에 짧게 앱을 여는 20~30대 직장인. 빨리 예약을 끝내고 싶어 함. </user>
  <screen> 결제 버튼을 누른 직후, 카드 한도 초과로 결제 실패. 자리는 10분 동안 유지됨. </screen>
</context>
```

## 제약과 레퍼런스
### 제약 조건
: 디자인 결과물은 화면에 들어가야 함. 길이/말투/내용을 숫자와 규칙으로 정하기
<img width="605" height="185" alt="Screenshot 2026-11-24 at 10 18 22" src="https://github.com/user-attachments/assets/b26bee67-f4f3-4ded-a21b-bfef396b5e84" />

### 레퍼런스 설명하기
: 특정 레퍼런스(앱, 이미지 등) 대신, 그 레퍼런스의 좋은 점을 **특징**으로 바꿔넣기
<img width="599" height="185" alt="image" src="https://github.com/user-attachments/assets/c3affdb1-9efd-47bb-b4ff-c0cc8f82a348" />

### 출력 형식
: 결과를 표로 출력받으면 비교하기 쉽고, 화면에 바로 넣을 수 있도록 **출력 포맷**까지 specify.
<img width="599" height="116" alt="image" src="https://github.com/user-attachments/assets/f70e36e3-c3c3-4c6c-b3a0-b362213ae346" />

> **TIP:** 맥락은 '블록' || 조건은 '숫자' || 형식은 '표' || 레퍼런스는 '특징'

## 화면 구성안
### 구성안 흐름
: 문구 대신 화면의 뼈대(영역/요소/상태)를 받는 프롬프트. 표로 받아야 Figma로 옮기기 쉬움.
1. 맥락 블록
2. 구성안 표
3. Figma로 옮기기
4. 화면 기준 검토

### 구성안 프롬프트 구조
```
<persona> 너는 10년차 UXUI 디자이너야. </persona>
<context> (맥락 블록 그대로 넣기) </context>
<task> 결제 실패 화면의 구성안을 써 줘. 위에서 아래 순서로. </task>
<constraints>
- 모바일 375px, 한 화면 안에 끝나게
- 주 버튼은 1개, 보조 버튼은 1개까지
- 상태: 기본 · 로딩 · 다시 실패
</constraints>
<format> 표: 순서 | 영역 | 들어갈 요소 | 상태·조건 </format>
```

- `<persona> / <role>` : AI의 역할
- `<context>`: 서비스, 상황, 맥락
- `<task>`: AI의 업무 (무엇을 해야하는지 전체적인 과업)
- `<constraints>`: 제약
- `<format>`: 출력 구조

> **TIP:** Plan모드로 계획을 세워 기획안/구성안을 세운 후 Auto모드로 화면 만들기

### 구성안 결과
: 받은 표의 번호를 화면에 그대로 옮기면 와이어프레임이 됨.
<img width="599" height="197" alt="Screenshot 2026-11-24 at 10 29 00" src="https://github.com/user-attachments/assets/b266fa25-7d81-467c-9c8a-959e8340ab91" />

**와이어프레임**: 앱/웹 화면에 콘텐츠와 버튼 등을 어디에 배치할지 **선과 박스**로 간단히 그린 **설계도**
<img width="648" height="219" alt="image" src="https://github.com/user-attachments/assets/c5c8af48-7a20-4b8e-8b81-b26b5cd79e1f" />

### 화면 챕처로 비평 받기 (Multimodal Prompt)
: 캡처를 함께 넣으면 AI가 화면을 읽고 비평함. 화면에 없는 것을 지어내는지 꼭 확인 필요.
<img width="583" height="163" alt="Screenshot 2026-11-24 at 10 30 58" src="https://github.com/user-attachments/assets/a3d9fa8f-2a2c-4c4e-abeb-c0fc599e0a7d" />

> **주의:** 문구만 받지 말고 **화면의 뼈대**도 같이 받기. 받은 뒤엔 꼭 화면 기준으로 검토하기.

## 2. Few-shot으로 품질 고정하기

## Few-shot
> 예시/레퍼런스를 주는 게 설명 10줄씩 쓰는 것보다 나음.

### Zero-shot vs. Few-shot
- One-shot: 원하는 결과 예시 **1개**를 주는 방법
- Few-shot: 원하는 결과 예시 **몇 개**를 주는 방법
- Zero-shot: 예시 없이 **설명만** 주는 방 (예시 X)
<img width="615" height="213" alt="Screenshot 2026-11-24 at 13 26 57" src="https://github.com/user-attachments/assets/822f9124-a9c5-48c3-9036-8f7dbad7bdd5" />

> **주의:** 한 번 잘 나온 건 운일 수도 있음. **여러 번 돌려서** 고른지 확인해야 함.

## 예시 고르기
### 좋은 예시 기준
1. 실제로 쓸 수준: 그대로 화면에 넣어도 되는 문구
2. 서로 다른 상황: 원인/상황이 다른 2~3개
3. 같은 형식: 제목/본문/버튼 구조를 통일

### 피할 예시
: 좋은 예시와 함께 피할 예시까지의 이유를 쓰면 경계가 분명해짐

## 예시 베끼기
: 예시가 하나 뿐라면/너무 비슷해지면, AI가 구조가 아닌 문장까지 따라할 수 있음.

### 반복 실행으로 확인
1. 5번 실행 (새 대화에서 같은 프롬포트를 사용하기)
2. 기준 3개로 체크 (길이/말투/구조)
3. 벗어난 이유 찾기 (예시? 조건? 맥락?)
4. 다음 버전으로 (바꾼 이유와 함께 기록하기)

# 3. 프롬프트 버전관리
## 왜 기록할까
: 잘 된 프롬프트도 기록이 없으면 다시 만들 수 없음.

### 기록이 없을 때
: 잘 나온 프롬프트도 기록이 없으면 다시 만들 수 없음.
1. 무엇을 바꿨는지 모름
2. 팀원이 같은 시행착오를 반복
3. 선택의 근거를 설명 못 함

> 프롬프트도 여러 **버전**으로 남기기!!!

## 버전 기록과 평가
### 버전마다 남길 4가지
: 바꾼 이유와 결과를 같이 남겨야 다음 사람이 이어서 고칠 수 있음.
<img width="664" height="200" alt="image" src="https://github.com/user-attachments/assets/077ed9b4-7e5d-437d-81cc-78043c28ba30" />

### 버전 기록 예시
예시 (결제 실패 문구 프롬프트를 한 표로 정리하면)
<img width="664" height="152" alt="image" src="https://github.com/user-attachments/assets/8a739ae1-5f92-4b58-a59c-8aa20f970c58" />

### 느낌 vs. 평가
: 모든 판단은 **근거가 있어야 함**
<img width="664" height="202" alt="Screenshot 2026-11-24 at 13 55 39" src="https://github.com/user-attachments/assets/9b8ad025-ec85-4886-890f-f6a8246e1d73" />

### 테스트 케이스 (Test Case)
: 버전마다 똑같이 넣어 볼 입력 5개. 흔한 상황과 예외 상황(edge case)을 섞기.
<img width="664" height="219" alt="Screenshot 2026-11-24 at 13 56 29" src="https://github.com/user-attachments/assets/0d36d7b0-d110-4578-9de7-727b1ac05cc1" />

### 루브릭 (Rubric)
: 점수 기준을 미리 적어 두면 누가 채점해도 비슷한 점수가 나옴.
<img width="664" height="165" alt="Screenshot 2026-11-24 at 13 57 20" src="https://github.com/user-attachments/assets/398d0687-75a3-462d-b382-161f90590a41" />

### 버전 점수표
: 같은 케이스/같은 루브릭으로 매긴 점수(0~5점 정도). 어떤 상확에서 약한지도 함께 확인 가능.
<img width="664" height="171" alt="image" src="https://github.com/user-attachments/assets/98f3d462-fb69-43bb-88f7-2bda0bd392a2" />

### AI 채점, 사람 확인 (LLM-as-a-Judge)
: 채점도 AI한테 맡길 수 있음. 대신 AI 점수는 후보이고, 사람이 확인한 점수만 기록함.
1. 루브릭 + 결과 넣기 (다른 도구에 넣으면 더 좋음)
2. AI가 점수를 부여 + 이유를 붙임 (케이스별로 표로 받기)
3. 사람이 2개 확인 (가장 높은/낮은 것)
4. 확정 점수 기록 (버전 기록표의 "결과를 비교")

## 라이브러리
### 템플릿 만들기 (Prompt Template)
: 바뀌는 부분을 {빈칸}으로 빼면 다른 화면 문구에도 다시 쓸 수 있음.
<img width="661" height="201" alt="Screenshot 2026-11-24 at 14 05 02" src="https://github.com/user-attachments/assets/6b7c7335-2066-426e-a12f-30c57c614f2f" />

### 템플릿 예시
: UX 카피 템플릿. 빈칸만 바꾸면 예약 완료/취소 화면 문구에도 쓸 수 있음.

```
<context>
<service> {서비스 이름 · 한 줄 설명 · 말투} </service>
<user> {누가 · 어떤 상황에서} </user>
<screen> {어느 화면 · 직전에 일어난 일} </screen>
</context>
<task> {문구 종류}를 {개수}세트 써 줘. </task>
<constraints> 제목 {n}자 · 본문 {n}자 · {말투} · 금지: {쓰지 않을 말} </constraints>
<examples> 좋은 예 {2~3개} / 피할 예 {1개 + 이유} — 예시는 구조만 참고, 문장은 새로 </examples>
<format> 표: 제목 | 본문 | 버튼 | 글자 수 </format>
```

### 팀 프롬프트 라이브러리
: 팀이 함께 쓰는 프롬프트 목록. 노션 표 하나로 시작하기.
<img width="661" height="162" alt="Screenshot 2026-11-24 at 14 07 29" src="https://github.com/user-attachments/assets/80e95107-e5b3-4915-8729-e5aad61f9a0f" />

# 11/23/2026

## 1. AI 도구 선정 기준

## AI와 디자인 워크플로우
: 프로덕트(앱/웹서비스 등)를 만들 때, 프로덕트 디자이너가 일하는 순서와 방식의 업무 프로세스

### Design Workflow 순서: **더블 다이아몬드**
: 확산하고(diverge) 수렴하는(converge) 관계의 반복
1. Discover
- **Emphathise(공감)**
* 데스크 리서치 (논문, 신문 등 업계 동향/경쟁사/외부 시장 요인 파악)
* 필드 리서치 (실제 사용자들과 니즈/불편함 파악)

2. Define
- **Define(정의)**
* 초기 인사이트
* 사용자 니즈 찾기 (affinity diagram / persona 등)
* 문제 정의

3. Develop
- **Ideate(발상)**
- **Prototype(모현 제작)**
* 아이디어 발산
* IA / Wireframe
* Prototype

4. Deliver
- **Test(테스트)**
* 검증 (AB Testing / Usability Testing / 클릭맵,히트맵 / 로그 이벤트 등)

<img width="507" height="247" alt="Screenshot 2026-11-23 at 10 15 31" src="https://github.com/user-attachments/assets/6ba3aec6-40ee-4b78-adcf-47be23578108" />

> **NOTE:** 가장 좋은 AI가 아니라 워크플로우 별로 필요한/적합한 AI를 찾기

### 단계별 AI 예시
1. Discover(발견)
: RAG 할 수 있는 LLM 사용이 유리함 | 언어 기반 LLM 사용
- 데스크 리서치 (검색형 AI) - 시장/경쟁 앱 조사와 출처
- 필드 리서치 준비 (텍스트 생성 AI) - 인터뷰/설문조사 질문지 초안
- 긴 자료 요약 (텍스트 생성 AI) - 리뷰, 녹취, 요약, 앞부분 확인

2. Define(정의)
: 생성형 AI | 텍스트 생성 LLM
- 어피니티 다이어그램 (생성형 AI) - 메모를 주제별로 묶은 초안
- 페르소나/고객여정지도 (텍스트 생성 AI) - 리서치 자료로 만든 초안
- 문제정의 문장 (텍스트 생선 AI) - HMW 문장 후보 여러 개 제시

3. Develop(개발)
: 생성형 AI | 코딩용 AI
- 아이디어 발산 (생성형 AI / 텍스트 생성 AI) - 해결안 후보 10개
- 화면 구성안 (생성형 AI) - 와이어프레임, IA 초안, 상태별 설계
- 화면 초안 (생성형 AI) - Figma Make 시안

4. Deliver(전달)
- 사용성 테스트 준비 (텍스트 생성 AI) - 태스크 시나리오 질문 초안
- 휴리스틱 평가 (텍스트 생성 AI / 멀티모달) - 캡처로 휴리스틱 점검
- 데이터 결과 정리 (텍스트  생성 AI / 멀티모달) - 결과 클러스터링, 1차 해석

> **NOTE:** 매일 특정 분야에 특화된 AI가 업데이트/바뀌기 때문에 주기적으로 확인 후 사용

> **TIP:** arena.ai 로 현재 관련 워크플로우에 맞춰 가장 적합하거나 효율이 좋은 AI 분류를 사용하기

### 워크플로우에 AI 더하기 (생성형 AI 예시)
<img width="698" height="479" alt="Screenshot 2026-11-23 at 10 24 27" src="https://github.com/user-attachments/assets/e87eb9b6-d4d1-4087-b6fa-f1b7945d2941" />

## 모델 차이 (모델은 왜 다 다르게 말하는건지)
### AI 모델이 답을 위해 사용하는 자료
- 학습한 지식 (어느 시점까지 무엇을 배웠나)
- 지금 넣은 자료 (대화/파일/컨텍스트)
- 생각하는 방힉 (바로 답할지(Instant), 단계를 거칠지(Deep Thinking))
- 검색 결과 (웹에서 찾아 온 최신 정보)

> **NOTE:** 모델이 추구하는 가치관/가치에 따라 그에 맞게 답변을 할 때도 많음 (e.g., X 내용을 보고 학습하는 Grok)

### 학습 시점 (**Knowledge Cutoff**)
: 모델은 특정 시점까지의 자료로 배움. 그 뒤의 일은 검색 없이는 모르거나 지어낼 수 있음.

> **주의:** 이럴때는 따로 검색을 켜고 물어볼 수 있다면 검색을 ON 해두는 것을 권장.

### 컨텍스트 창 (**Context Window**)
: AI가 한 번에 읽을 수 있는 양. 넘치면 앞부분을 놓치거나 줄여서 읽음.
<img width="666" height="216" alt="Screenshot 2026-11-23 at 10 34 00" src="https://github.com/user-attachments/assets/df692b50-a406-455c-8b0b-1d0e3bef6a02" />

> **주의:** 길거나 내용이 많은 프롬프트/자료를 첨부했다면 쪼개서 넣어야 모든 정보가 읽히고 누락 정보가 없어질 확률 높아짐.

### 추론 모드 (**Reasoning**)
: 답하기 전에 단계를 거쳐 생각하는 모드. 조건이 많은 일에 강하지만, 속도가 느리고 한도를 더 씀.
- Instant vs. Deep Thinking mode in ChatGPT
- Fable vs. Haiku in Claude

### 검색 결과 (**Search Results**)
: 출처 없는 그럴 듯한 답을 낼 수 있기 때문에 출처 밝힐 수 있게끔 설계하는 게 중요함.

### 재료별 확인 법
: 답이 이상하면 모델을 바꾸지 전에 AI한테 넣거나 AI가 쓴 재료부터 확인
<img width="688" height="191" alt="Screenshot 2026-11-23 at 10 35 39" src="https://github.com/user-attachments/assets/5e307cc3-9aa5-4ae7-b0b9-d1795122788d" />

## 선정 기준
1. 출력 품질 (문장의 자연스러움, 사실 정확도)
: 결과물이 바로 쓸 만한가
2. 컨텍스트 길이 (긴 인터뷰 녹취, 기획서)
: 한 번에 읽고 기억하는 양
3. 멀티모달 (화면 캠처 읽기, 이미지 생성)
: 글 외의 입력/출력
4. 검색 연동 (경쟁 앱 정책 조사)
: 최신 정보와 출서
5. 비용 (하루 사용 횟수)
: 무료 한도와 유료 가격
6. 데이터 정책 (학습 사용 설정, 회사 규정)
: 입력한 내용이 어디에 쓰이나

## 기준 중돌
: 6가지 선정 기준을 다 만족하는 도구는 드물기 때문에 **이 일에서 없으면 안되는 기준**으로 정함.
예: 고객 문의 5,000건 분석할 때 컨텍스트 길이 vs. 데이터 정책 이라면 데이터 정책을 먼저 보고 우선시하기

### 도구 고르는 순서
: 결과를 보기 전에 기준을 정하고, 결과로 고른 이유를 남기기
1. 할 일 한 줄로 (무엇을 만들지 한 문장으로 정리)
2. 핵심 기준 1-2개 (없으면 안 되는 기준 세우기)
3. 후보 2-3개 실행 (같은 과업 / 같은 프롬프트 비교해가며 진행)
4. 선택과 근거 기록 (결과로 고른 이유)

## 2. 디자인 태스크별 도구 매칭

## 디자인 태스크
### 디자인 태스크 4종 (디자이너가 AI에 맡기는 일 4가지)
1. 리서치: 자료 찾고 요약
2. 카피라이팅: 화면 속 문구 쓰기
3. 시안 생성: 화면/프로토타입 초안
4. 데이터 분석: 숫자에서 패턴 찾기

### 태스크별 핵심 기준
: 4종 태스크마다 먼저 볼 기준이 다름
- 리서치: 검색 연동 (출처 링크가 열리고 내용이 맞나)
- 카피라이팅: 출력 품질 (톤/글자 수/맥락을 지키나)
- 시안 생성: 멀티모달 (화면으로 나오고 고칠 수 있나)
- 데이터 분석: 컨텍스트 길이/데이터 정책 (파일 전체를 잘 읽나, 개인정보는 없나)

## 태스크별 시연
### 리서치
: 자료 조사는 출처가 붙는 **검색형 답**이므로, 링크를 열어 원문과 맞는지 확인
<img width="501" height="161" alt="Screenshot 2026-11-23 at 13 18 25" src="https://github.com/user-attachments/assets/64af1f8b-c410-4e25-96d1-da65a6ae3bfb" />

### 카피라이팅
: 같은 요청을 도구 2-3개에 넣고, 특정 브랜드/서비스/제품의 **(라이팅)원칙/조건**을 지켰는지도 비교
<img width="501" height="128" alt="image" src="https://github.com/user-attachments/assets/a04ec796-875d-40b3-8007-59518ed648a4" />

### 시안 생성
: 화면 초안은 프로토타입 툴 AI이기 때문에, **결과는 시작점**일 뿐, 기준에 맞게 사람이 다듬기
<img width="501" height="90" alt="image" src="https://github.com/user-attachments/assets/07ac6994-69d3-48f7-853b-e50329c061fa" />

### 데이터 분석
: 파일 분석은 파일을 통째로 읽는 도구이므로, 숫자는 **계산 방법**까지 받아서 확인
<img width="501" height="119" alt="image" src="https://github.com/user-attachments/assets/abd3c7df-25ca-4874-823c-4b54df0ebc66" />

## 섞어 쓰기
### 도구 넘겨주기
: 한 도구에서 끝내지 않고 유기적으로 상황에 맞는 AI에게 또 연결해서 맡김
### 유기적 절차
1. 조사 (검색형 AI -> 출처 붙은 규정 표)
2. 정리 (텍스트 생성 AI -> 문구 원칙 3줄)
3. 문구 (텍스트 생성 AI -> 결제 실패 문구 후보)
4. 화면 (Figma Make -> 결제 실패 화면 초안)

> **NOTE:** Version Update로 각 절차별 단계마다 바꾼 점, 진행한 점 표/문서로 기록하고 정리하기 => 그래야 이전 버전으로, Roll-back으로 넘어갈 수 있음

## 3. 도구 조합 워크플로우

## 워크플로우 (4단계)
1. 리서치: 문제와 사례 모으기
2. 설계: 흐름/구조/문구 정하기
3. 프로토타이핑: 화면으로 만들기
4. 검증: 사용자/팀과 확인하기

### 단계별 도구 배치
<img width="492" height="156" alt="image" src="https://github.com/user-attachments/assets/8d5abe61-f6cf-4bf7-a4ed-08232a3ffdf3" />

## 입력과 출력
: 각 워크플로우 단계의 출력은 다음 단계의 입력이 되도록 유기적으로 설계하기
<img width="497" height="88" alt="image" src="https://github.com/user-attachments/assets/6f86a1dd-fe70-4dd0-a3c3-1080f9d38881" />

> **주의:** 끊긴 흐름으로 개연성/맥락에 어긋나지 않게끔 각 단계가 연결되도록 기록
<img width="497" height="159" alt="Screenshot 2026-11-23 at 14 32 29" src="https://github.com/user-attachments/assets/e8e37738-9f26-4c45-96e6-2fb8d3c18c22" />

## 검토 지점
### Human-in-the-loop
: AI 결과가 다음 단계로 넘어가기 전, 미리 검수 영역을 정하기; **AI 작업을 중간중간 검수하는 사람**.
1. 사실 확인 (출처/숫자가 맞는지)
2. 맥락 확인 (우리 서비스/영향을 받을 사용자에게 맞는지)
3. 결정 (무엇을 채택/버릴지)

> **TIP:** AI는 후보를 만들 뿐, 채택은 사람이 근거로 정함. 따라서 **맥락**이 중요함

### 다이어그램 예시
<img width="702" height="234" alt="Screenshot 2026-11-23 at 14 36 07" src="https://github.com/user-attachments/assets/5056029d-274b-4e37-97b4-a49f8ce24251" />

## 실습
<img width="3300" height="756" alt="image" src="https://github.com/user-attachments/assets/74b92412-54eb-4fc2-94f4-3825f14652d2" />
