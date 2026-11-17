# Week 3 (11/09 ~ 11/13)

# 11/13/2026

## Usability (사용성)
: 사용자가 특정 상황에서 제품/서비스를 이용해 목표를 **효과적/효율적으로, 만족스럽게 달성할 수 있는 정도** // 사용자가 제품/서비스를 얼마나 쉽게 사용할 수 있는가
예) 예약하려는데 예약완료 10분이 걸렸다 -> 효과 O, 효율 X

### Usability Measurement Criteria (사용성 측정항목)
- Efficiency (효율성)
- Learnability (학습 용이성)
- Memorability (기억 가능성)
- Error (에러)
- Satisfaction (만족)

### Usability Measurement Methods
- 행동 (하는 것을 봄)
  - 정성 (Qualitative): 사용성 테스트 (UT), 필드 관찰
  - 정량 (Quantitative): A/B 테스트, 로그/클릭 분석
- 태도 (말하는 것을 들음)
  - 정성 (Qualitative): 사용자 인터뷰, 포커스 그룹
  - 정량 (Quantitative): 설문조사
- 사용자 없이 진행할 수 있는 것: 휴리스틱 평가 (디자이너가 원칙으로 화면을 점검) -- 가장 빠르게 문제 후보를 찾는 방법

### Heuristic Evaluation (휴리스틱 평가)
: 사용자 없이 빠르게 문제 후보를 찾는 방법. 정해진 원칙(휴리스틱) 10가지로 화면의 문제를 찾는 방법
참가자: 디자이너/평가자 3~5명 (80%까지 효과를 끌어올릴 수 있는 가장 적합한/optimal 수)
+ 장점: 빠름, 비용이 적음
- 단점: 가설을 만드는데에만 사용 가능 (가설을 증명/실험하는 것은 UT(사용자 테스트)

## Nielsen 10 Heuristics
: Usability(사용성) 점검하는 특정 기준
1. Visibility of System Status (시스템 상태 가시성)
   : 서비스가 지금 뭘 하고 있는지 적절한 피드백으로 바로 알려줘야함
   - Component의 State를 활용해 사용자의 액션에 따른 현재 상태(로딩/완료/실패 등)를 보여주기
2. Match between the System and the Real World
   : 사용자에게 익숙한 언어/현실과 같은 형태로 보여줘야함
   - 회사에서 쓰는 줄임말/전문용어가 아닌 사용자가 쉽게 이해할 수 있게끔 설계
3. User Control and Freedom
   : 실수로 들어간 상황에서 사용자가 바로 빠져나올 비상구(취소/되돌리기)가 보여야함
   - 사용자가 잘못 들어간 페이지에서 뒤로 갈 수 있거나, 취소할 수 있는 버튼 설계하기
4. Consistency and Standards
   : 플랫폼이나 서비스 내부에서 디자인과 규칙을 유지해야함
   - **외부 일관성**: 일관적인 사용자 경험을 제공하기 위한 플랫폼/업계의 관습
   - **내부 일관성**: 사용자가 혼란스럽지 않게 한 플랫폼 내 제품의 인터페이스나 정보 제공에 일관성이 있어야 함 (e.g., 컬러/컴포넌트의 구성/화면 규칙)
5. Error Prevention
   : 친절한 오류 메시지 < 실수가 애초에 생기지 않게 아예 막는 디자인이 먼저
   - 비용이 큰 오류를 미리 보여주기 (e.g., 버튼을 미리 Disabled 시킨다던지)
6. Recognition rather than Recall
    : 사용자가 앞 화면의 정보를 외우지 않게, 필요한 정보를 화면에 보여 줘야함
    - 사용자가 고른 것/지난 행동을 보여주는 것 (e.g., 지난 검색 기록 보여주기, 회원가입 중 했던 단계/기록 보여주기)
7. Flexibility and Efficiency of Use
   : 처음 쓰는 사람과 익숙한 사람 모두 빠르게 쓸 수 있게, 지름길을 함께 둬야함
    - 지름길은 보통 익숙한 사람에게, 처음 쓰는 사람에게는 차근차근
    - 지름길도 디자인 시스템에 일관되게끔
8. Aesthetic and Minimalist Design
   : 지금 필요 없는 정보가 필요한 정보를 가리지 않게 해야함
    (미니멀 디자인은 화면의 목적을 먼저 보이게 하는 것)
    - 화면에 사용자가 집중해야 하는 부분을/페이지의 목적을 먼저 보이게 하는 것 / 우선시 하도록 화면 디자인
9. Help users Recognise, Diagnose, and Recover from Errors
   : 오류가 아면 쉬운 말로 원인을 알려 주고, 해결 방법을 함께 제안해야함
    - 어떤 오류인지, 어떻게 해야 해결할 수 있는지, 실제 사용자가 이해할 수 있는 언어로 알려주기 (사용자가 한번에 이해하기 어려운 오류 코드 등은 안쓰는게 나음)
10. Help and Documentation
    : 필요하면 그 순간/그 자리에서 도움말/가이드 문서를 쉽게 찾을 수 있어야함 (설명 없이 쓰이는 게 가장 좋긴함)
    - 가이드 및 도움을 쉽게 구할 수 있도록 버튼 위 hovering 도움말이라던가, 도움말 옵션 찾기 쉽게 배치

> **중요:** Heuristic은 꼭 지켜야 하는 법칙이 아니라 판단 기준일 뿐. 따라서 휴리스틱을 몇 가지 위반한다고 해도 상황에 따라 그대로 두기도 함.

# 디자이너 UX 법칙
> **주의:** 꼭 지켜야 할 규칙은 X (설계를 설명하는 근거) -- 이를 토대로 UT등 사용자와 테스트 진행

## Fitts's Law (피츠의 법칙)
: 목표까지 거리가 멀고, 크기가 작을수록 누르는 데 오래 걸림.
- Thumbzone (엄지가 닿기 편한 - 어려운 화면 부분)을 고려해 행동을 유도하고픈 버튼은 엄지와의 거리를 좁히고 크기는 크게
- 정보의 위계 (Hierarchy): **자주 눌리는** 버튼은 Fitts's Law를 고려해서 크게 손가락과 가깝게 위치하도록 설계

## Hick's Law (힉의 법칙)
: 선택지가 많고 복잡할수록 결정하는 데 오래 걸림.
- 선택지를 줄이거나 '추천'을 띄우고 전체보기 옵션을 따로 만들기 (Tertiary 위계 등으로 설정하면서)
- 선택지를 무작정 줄이기 보다는 고르기 쉽게 정리함
  - 묶기 (비슷한 것끼리 카테고리로)
  - 단계 나누기 (한 화면에 한 가지 결정)
    > **주의:** 이전 단계들이 잊히지 않게끔 설정
  - 추천 먼저 (많이 고르는 것을 앞에)

## Jakob's Law (제이콥의 법칙)
: 사용자는 대부분의 시간을 다른 서비스에서 보냄. 그래서 새 서비스도 익숙한 방식으로 움직이길 기대함.
- 유사한 서비스 안에서 시간을 보내고 있기 때문에 다른 비슷한 서비스에 맞춰서 디자인 설계
- 처음 쓰는 앱이더라도 조작방법과 탭바 구성/순서/위치 등을 유사하게 두기
- 익숙한 패턴 위에 우리 서비스의 차이/포인트만 더하기
> **TIP:** 꼭 새로워야 하는 게 아니라면, 사용자가 이미 아는 방식을 따라야함 (꼭 새로워야 하는 것이라면 그에 맞는 특장점이 따라야함)

## Miller's Law (밀러의 법칙)
: 사람이 한 번에 기억하는 양은 적음 (평균 7±2개). 정보를 덩어리로 나누면 기억하기 쉬움.
- 긴 정보는 덩어리로 나누는 것 (e.g., 전화번호를 **'-'** 로 나누는 것 // 계좌번호를 숫자 4개씩 **덩어리로** 나눠 쓰는 것)

## Gestalt Theory (게슈탈트 원리)
: 사람은 화면을 낱개가 아니라 묶음으로 봄. 간격/모양/영역이 묶음을 정함.
- 간격/색/박스로 무엇이 한 묶음인지, 같은 객체처럼 보이도록 설계하기

### Law of Proximity (근접 (가까이 있으면 한 묶음))
- 같은 영역끼리 **확실하게 좁히고** 관련 없는 영역끼리 **확실하게 넓히기**
### 유사 (모양/색이 같으면 같은 역할)
### 공통 영역 (같은 박스 안이면 한 묶음)

## Heuristic Evaluation (휴리스틱 평가)

### Heuristic Evaluation Steps/Process
1. 범위/태스크 정하기: 어떤 화면에서 사용자가 어떤 행동을 할지 정하기
2. 각자 평가: 평가자 3~5명이 따로 각자 평가 (한 사람만 하면 놓치는 부분이 있고, 너무 많으면 산으로 가거나 절차가 길어질 위험이 있으인 3~5명이 적합)
3. 합치기: 겹치는 문제를 묶고 다른 의견 표시
4. 심각도/개선안: 무엇부터 어떻게 고칠지 우선순위와 해결책 정하기

### User Flow (유저 플로우)
: 태스크를 위해 사용자가 거쳐야 하는 단계들
- Happy case (의도한 결말에 다다랐을 때)
- Edge case (중간에 의도하지 않은 실패가 생겼을 때 -- Edge case exit 방법도 설계해야 사용자가 자유롭게 컨트롤 할 수 있도록 보장)

### IA (Information Architecture)

## Report & Severity (리포트와 심각도)
: 평가지 원칙마다 심각도(0~4)를 매기고, 팀 평균을 색으로 칠하면 어떤 문제를 우선시해서 해결해야할지 보임

### Severity Rating (심각도 등급)
- 0: 문제 아님 (사용성 문제로 보기 어려움)
- 1: 겉모양 문제 (시간 여유가 있을 때 고침)
- 2: 작은 문제 (낮은 우선순위)
- 3: 큰 문제 (높은 우선순위)
- 4: 치명적 문제 (출시 전 반드시 고침)

### 심각도 판단 기준 (3 가지)
1. 빈도 (얼마나 자주 생기나)
2. 영향 (생기면 얼마나 막히나)
3. 지속성 (한 번 알면 피할 수 있나)
> **TIP:** 기준 중 3개 다 해당이면 Severity=4, 1-2개면 Severity=2~3, 0-1개면 Severity=0~1로 각 원칙마다 심각도 점수 매기기

### Report 구성
- 문제 당 Row
- PM/개발자 등이 Agile environment에서 읽고 바로 고칠 수 있게 씀
  - 숫자 넘버링
  - 화면 (어떤 화면에서 생긴 문제)
  - 문제 (진단 문장: 어떤 문제가 생겨서 사용자가 어떻게 행동하고 있는가)
  - 위반 원칙 (Nielsen's 10 Heuristics 중 택)
  - 심각도 (숫자: 0~4)
  - 개선안 (어떻게 해당 문제를 고칠 수 있을지, 어떤 요소 및 개선 방안을 추가해야할지)

#### 좋은 리포트
: 읽는 사람이 다시 묻지 않아도 한 번에 이해할 수 있는 것 (읽자마자 고칠 수 있는 것 -> 팀 업무 효율 높일 수 있음)
> **TIP:** AI 초안 검증으로 해당 화면 캡처로 문제, 태스크, 10개 원칙을 첨부해 프롬포트로 넣고 후보를 빠르게 뽑음, 대신에 화면에 없는 문제를 지어내기도 하므로 채택은 사람이 근거로 채택/판단해 정리하는게 필요

# 11/12/2026

## Figma Make
: 프롬프트로 동작하는 프로토타입/웹앱을 만드는 도구

사용하면 좋을 때:
- 빠른 검증
- 빠른 시안
- 빠른 아이디어

## 프롬프트 구조
추천 구조:
- 목표
- 맥락
- 화면 요소
- 제약
- 완성 기준
> **TIP:** (레퍼런스)이미지/(피그마에선)맥락에 맞는 프로토타입 자체를 넣는 것을 권장

예시:
```
목표 : 모바일 앱의 클래스 상세 화면 1개를 만들어 줘. 사용자가 클래스 정보를 보고 바로 예약하게 하는 화면이야.
맥락 : 모임핏은 동네 운동 클래스 예약 앱이야. 퇴근 후 운동을 찾는 20~30대 직장인이 써. 첨부한 파일 속 예약 플로우와 같은 흐름이야.
화면 요소 : 사진, 클래스명, 일정·장소, 남은 자리(예: 남은 자리 3), 가격, 환불 규정 요약, 하단 "예약하기" 버튼을 넣어줘.
제약 : 모바일 390×844 한 화면으로 만들어 줘. 메인 색은 #0057FF 하나, 글꼴은 1종만 쓰고 이모지 아이콘은 쓰지 마. 없는 리뷰·평점은 만들지 마.
완성 기준 : 예약하기를 누르면 일정 선택 화면으로 넘어가면 완성. 남은 자리가 0이면 버튼이 비활성으로 보여야 함.
```
## 대화형 수정
:v0 -> v3 수정 (조금씩 advance해서)
무엇을 / 어떻게 바꾸고 / 무엇을 그대로 둘지만 쓰기

- v0: 첫 생성
- v1: 구조
- v2: 상태
- v3: 문구

### 디자인 맥락 주기
- Make 파일에서 플러스 누르면 ```Add context``` -> Connectors등의 MCP로  연결
- 프레임 등을 레퍼런스로 첨부
- Make에서 생성된 1차 초안 프로토타입 자체를 위에 Comment 남겨서 실시간 정확한 부분 피드백 가능

## 검수 기준
: AI가 만든 화면에 문제 지점을 번호로 표시 (빨간 번호 버튼 레이블)

## 보정 순서
: 뼈대부터 고쳐야 다시 고칠 일이 없음. 문구는 화면이 정리된 뒤 마지막에
1. 구조 (Auto Layout, Layer Name)
2. 컴포넌트 교체 (Instance/Icon으로 바꾸기)
3. 상태 (Disabled/Pressed/Error 등)
4. 문구 (지어낸 수치, 사실 확인 등)

## 기록하기
### 전/후 기록표
: 프로젝트에서 Rollback하는 (전 버전으로 돌아가는) 경우 다수 있고, 이전에 기록 및 작업 흐름을 전반적으로 파악할 수 있게끔

# 11/11/2026

## 상태 전환 (Toggle) 방식
1. 화면 복제 (화면 전체를 전환할 때 사용)
2. Interactive Component (화면의 **일부**만 (요소가) 바뀔 때 사용)

## Interactive Component (화면 말고 요소끼리 Transition)
1) Main Components 2가지 Toggle Variant 묶고 Rename each variant state
2) Prototype 탭에서 Main Component interaction 한 가지 추가 (**Smart Animate**)
3) Interaction 추가된 Main Component의 **Instance**로 화면에 추가

> **주의:** 같은 Variant 세트 안에서만 연결 가능
> **주의:** Smart Animate 쓸 때 연결 될 아이콘들 이름은 하나로 통일

### Variant Trigger별 전환
1. On-tap
2. While hovering (Mobile에서는 해당 없음)
3. _

### 사용 예시 & 배치
1. 토글/체크박스
2. 찜 버튼
3. 탭 전환
4. 수량 스테퍼

> 정리: 화면의 Transition/Flow (흐름): Navigate to로 잇고, 화면 안 Component 자체의 상태 변화: Interactive Component의 Instance로 잇기
> **주의:** After delay는 화면 흐름에서만 사용

## iOS vs. Material 3
- iOS: 애플 (Apple) Design System
- Material 3: 안드로이드 (Google) Design System

### 버튼 vs. 링크
- 실행은 버튼,

### 체크박스
- 전체선택을 안했을 때는 전체선택의 체크박스에 ```-``` 표시

### 라디오 버튼
: 여러 개 중 딱 하나만 고를 때

### 토글/스위치
: 신속성으로 바로 반영 되어야 하는 것 / Boolean

### 드롭다운/셀렉트
: 선택지가 많아서 화면에 다 펼쳐두기 어려울 때

### 칩
: 필터/태그/추천 검색어처럼 가볍게 고르거나/필터링하거나 지울 때
- 칩은 누를 수 있음
- 누를 수 없는 상태는 백지

### 스테퍼
: 정확한 수량/인원의 작은 범위의 숫자를 정확하게 바꿀 때
- 최솟값/최댓값에서는 -/+ 의 Disabled 상태 각각 사용

### 슬라이더
: 정확한 숫자보다 대략적인 정도/범위 고를 때

## 비교
- 앱 바 vs. 탭 바
- 탭 vs. 탭 바
  : 페이지 안에서 이동하는 것 (탭) vs. 페이지를 오가며 이동하는 것 (탭 바)
- 탭 vs. 세그먼트
  : 둘 다 같은 페이지 안에서 이동하지만 다른 묶음 (탭) vs. 같은 묶음/데이터 안에서 다른 보기 (세그먼트) {대괄호 탭 vs. 안에 있는 소괄호 세그먼트}
- 햄버거 vs. 케밥
  : (안드로이드에서는 햄버거를 많이 쓰 되 iOS는 X)

## 이동

### 앱 바
- 페이지 맨 위에 나타나는 Title, Navigation controls, Quick actions 등 표기하는 부분
- 위에 나타나는 부분은 **top navigation bar**로도 자주 불림

### 탭 바
- 아래 중요한 옵션 2~5가지는 **bottom navigation bar**로도 자주 불림

### 탭
- 

### 세그먼트 컨트롤
- 페이지 하나 안에서 모든 걸 보여줄 수 있음 (페이지 당 2~5개가 적당)

### 햄버거 메뉴
- 줄 3개 심볼의 숨은 메뉴 (iOS는 숨은 메뉴 X -- 탭 바 권함)
- 중요한 메뉴는 햄버거로 숨기지 X

### 케밥 메뉴 / More menu
- iOS: 가로 점 3개
- 안드로이드: 세로 점 3개
- 중요한 메뉴는 케밥으로도 숨기지 X

### FAB (Floating Action Button)
- 화면에서 가장 중요한 행동 1개 옵션 버튼 (e.g., ```만들기```)
- 대신 중요한 옵션이 2+개라면 FAB 누르면 옵션 버튼 위로 더 뜨게 (이때, 기존 FAB버튼은 리스트 닫기 옵션으로 바뀜)

### 아이콘 버튼
- 아이콘이 버튼이 되는 경우
- iOS, Android는 공유 아이콘이 다름
- 아이콘이 작아도 버튼 자체는 44~48px 사이로 누를 수 있는 touch target 영역 넓히기


## 비교 (알림/피드백)
- 토스트 vs. 스낵바
  : 알림만(토스트), 알림+유저가 즉각으로 실행할 수 있는 행동까지(스낵바)
- 배너 vs. 토스트
  : 남아있음(보통 X랑 같이 뜸)(배너), 잠깐 뜨고 사라짐(토스트)
- 모달 vs. 바텀시트
  : 유저가 즉각적으로 멈추고 확인을 해야 화면을 벗어날 수 있음(모달); 중요도 높음, 흐름을 유지하며 배경(과 호환돼서) 눌러도 벗어날 수 있음(바텀시트); 중요도 비교적 낮음
- 툴팁 vs. 팝오버
  : 짧은 설명(툴팁), 작은 메뉴/설정 hover하면 생기는 간단한 설명(팝오버)
- 툴팁 vs. 코치마크
  : 필요할 때마다 설명(툴팁), 유저가 처음 쓸 때 안내(코치마크)
- 스피너 vs. 스켈레톤
  : 언제 끝날지 모름(스피너), 로딩되기 전 콘텐츠 모양을 미리 보여주는 것(스켈레톤)
- 프로그레스 바 vs. 스텝
  : 유저가 기다릴 때 현황을 보여주기 위해 비율로 진행(프로그레스 바), 같은 이유로 단계로 진행 상황(스텝)
- 배지 vs. 칩
  :

### 토스트
### 스낵바
### 배너
### 모달
- 흐름이 끊길 수 있음
- 대신 유저가 꼭 interact 해야하는 부분만 모달로 (모달 내 옵션 중 꼭 택 1 해야만 다음으로 넘어갈 수 있는 것)
### 바텀시트
- 배경과 상호작용 할 수 있는 바텀시트 있음
### 툴팁
### 팝오버
### 코치마크
- 유저가 처음 쓸 때 보여주는 가이드
### 배지
- 새 알림/안 읽은 개수처럼 유저한테 간단한 표시로 상황을 전달하는 것
### 스피너
### 스켈레톤
### 프로그레스 바
### 스텝 인디케이터
- 단계별로 유저가 사용하고 있을 때 총 몇 단계 중 어떤 단계에 있는지 등을 표시해주는 것

## 비교 (콘텐츠 표시)
- 카드 vs. 리스트
  : 이미지 중심(카드), 글자 중심(리스트)
- 아바타 vs. 썸네일
  : 사람/계정의 이미지(아바타), 콘텐츠 미리보기 이미지 (예: 카드 내에 사진) (썸네일)
- 배너 슬라이더 vs. 캐러셀
  : Hero (페이지의 메인 사진 한장)영역이 한장 씩 자유롭게 움직일 수 있는 것(배너 슬라이더), 이미지 여러장이 한번에 보이면서 자유롭게 움직일 수 있는 것(캐러셀)

### 카드
- Elevated | Filled | Outlined
- Stacked Card | card/vertical (세로로 쌓인 이미지 중심 리스트)
- card/horizontal (가로로 쌓인 이미지 중심 리스트)
### 리스트
- 글 중심의 리스트
### 아바타
- 
### 썸네일
- 서비스마다 쓰는 썸네일 **비율**이 중요함
- 비율을 통일하고, 이미지가 없을 때 대체 이미지가 필요
### 배너 슬라이더
- 꼭 알려주고 싶은 이미지 (Hero, Full-screen 도양 등) 한 장을 크게 보여주는 것
- 이미지 슬라이더/롤링 배너로도 불림
- indicator 현재 전체 이미지 중 몇 번째 이미지인지 보여주는 표시도 아래에 추가
### 캐러셀
- 여러 장씩 한번에 넘길 수 있는 것

## Figma AI
### 기능 리스트
1. 반복 작업 단축
   - 글/레이어 (이미 만든 화면을 빠르게 정리)
     - ```Rename layers```
     - ```Suggest auto layout``` (대신 AL에 들어갈 요소랑 순서는 수동으로 맞춰서 돌리기)
     - ```Translate to...```
     - ```Replace content```
   - 이미지 (있는 사진 손보기)
     - ```Remove background```
     - ```Boost resolution```
     - ```Erase object```
2. 생성형
   - 글/레이어 (없던 화면/연결/문구를 새로 만들기)
     - ```First Draft```
     - ```Add interactions```
     - ```Rewrite this```
   - 이미지 (없던 이미지를 새로 만들기)
     - ```Make image```
     - ```Edit image```
     - ```Expand image```

> 하단 Tool Bar에서 ```Actions``` 옵션
> **주의:** 기능에 따라 AI 크레딧 쓰는 정도가 갈라짐
> **TIP:** Figma AI는 효율성을 높이고 브레인스토밍/초안 작성할 때 사용하되 회사 디자인 시스템에 맞는지 검수하고 판단하며 퀄리티를 높이는/수정하는 건 인간 디자이너로서 해야할 일

## AI 기능 쓰는 순서 (Iteration)
1. 범위 고르기
   - 작은 범위 (e.g., 카드 1개, 영역 1개)
2. AI 실행
3. 검수
4. 고치기
5. 기록

# 11/10/2026

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
   - After delay (버튼이 아닌 ***화면 프레임***에 걸기)
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
> **TIP:** 매 페이지마다 반복되는 Flow/Transition 화살표를 줄이고 싶다면 (e.g., Tab-bar) Main Component로 따로 설정한 후에 반복될 각 Transition을 Main Component에서만 정의 (화살표 잇기). Instance는 그대로 따라감. Alternatively, 각 버튼을 Main Component로 설정하고 Main Components를 다 묶어서 Variant로 설정. 이후 Main Components 묶음(Variant)을 각 페이지의 Instance로 붙여넣기.

막힌 경로 (Dead end)
: 다음 연결되는 페이지가 없거나, 백을 할 수가 없는 구조

> **TIP:** Preview에서 화면 내에 누를 수 있는/상호작용 할 수 있는 요소를 한번에 확인하려면 화면 밖 영역을 클릭하면 hover상태로 누를 수 있는 버튼 표시해줌
> **TIP:** Preview에서 ```Share Prototype``` 선택지


## Smart Animate (Animation)

### Animation 종류
   - Instant (바로 바뀜)
   - Dissolve (서서히 겹치며 바뀜)
   - Move in (새 화면이 위에 덮임)
   - Push (새 화면이 밀어냄)
   - Smart Animate (**같은 이름 레이어**를 (웬만하면 같은 Layer 순서) 자동으로 트래킹해 움직임 (e.g., 찜 버튼/'장바구니에 추가됐어요' 팝업))
> **Note:** Smart Animate가 제대로 안 씌워지면 Dissolve로 대신하기

### Easing & Duration
: Easing은 속도가 변하는 모양, Duration은 걸리는 시간. 앱 화면 전환은 200~300ms가 무난함.

#### Easing 종류
   - Linear (기계적)
   - Ease out (들어오는 화면) -- 가장 많이 쓰는 Easing 종류
   - Ease in (나가는 화면)
   - Ease in and out (제자리 변화)
   - Spring (스프링처럼 조금씩 튕기도록)

## 바텀시트 Overlay
: 지금 화면
- Transition을 Open overlay로 위에 얹어질 요소에 Transition 설정
(e.g., **toast** -- 유저가 뭘 했는지 확인해주는 UI (예: '찜 목록에 담았어요'))

## Scroll (Behaviour)
- Vertical/Horizontal/Both
* Vertical (세로 스크롤) {e.g., 클래스 상세, 세로 체크리스트)
> **주의:** _Parent frame에 씌워_ 줘야하는데 Parent frame의 _height_ < Child frame 내용 _height_ 여야 Vertical Overflow로 스크롤 가능
* Horizontal (가로 스크롤) {e.g., 추천 카드 목록, 강사 사진)
> **주의:** _Parent frame에 씌워_ 줘야하는데 Parent frame의 _width_ < Child frame 내용 _width_ 여야 Horizontal Overflow로 스크롤 가능
* Both (양쪽 스크롤) {e.g., 지도, 큰 표}
> **주의:** _Parent frame에 씌워_ 줘야하는데 Parent frame의 _height & width_ < Child frame의 _height & widgth_ 여야 Both Overflow로 스크롤 가능

- Fixed/Sticky/Overflow
: Overflow는 프레임이 스크롤되는 방향, Position은 그 안 요소가 움직이는 방식, 스크롤은 내용이 프레임보다 길 때만 생김
* Fixed: 한 자리에만 고정
> **주의:** AL 요소는 Fixed X (대신 Ignore AL 상태면 Fixed 가능해짐)
* Sticky: Scroll과 함께 어느 한 순간 화면 모서리에 붙는 상태
> **TIP:** 예를 들어 Top에 고정하려면 Constraints를 Top으로 두고 Sticky scroll 옵션 선택
> **TIP:** status-bar 때문에 sticky 요소가 Top일 때 가려진다면 요소의 top padding만 status-bar height 만큼 늘리기


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
