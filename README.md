# Product Design TIL

## 11/02/2026
### Figma Auto Layout & GUI vs. Product Designer 정리

#### 1. Figma Auto Layout 기본

##### 간격(Spacing)
- 모든 간격값은 **4의 배수**로 설정 (4, 8, 12, 16, 20, 24 …)
- 일관된 리듬을 만들고 개발 핸드오프 시 수치가 깔끔해짐

##### Wrapping 옵션
- Auto Layout의 **Wrap** 옵션을 켜면 가로 공간이 부족할 때 자식 요소가 다음 줄로 넘어감
- 태그, 칩, 카드 그리드처럼 개수가 가변적인 요소에 유용

##### Overflow (스크롤)
- 방향: **Horizontal** / **Vertical**
- 작동 조건: **부모 프레임이 자식(콘텐츠)보다 작아야 함**
  - 부모 프레임 ≥ 자식 프레임 → 넘칠 내용이 없으므로 스크롤이 작동하지 않음
  - 부모 프레임 < 자식 프레임 → 넘친 영역이 스크롤됨

##### Ignore Auto Layout (Absolute Position)
- 자식 요소 **위에 겹쳐 올리는 요소**(배지, 플로팅 버튼 등)는 해당 요소에 **Ignore auto layout** 적용
- Auto Layout 흐름에서 빠져 자유롭게 위치 지정 가능
- 화면 상단·하단에 고정해야 한다면 Ignore 후 **Top / Bottom constraints** 설정

##### Fill Container로 하단 고정
- `content` 프레임의 높이(H)를 **Fill container**로 설정
- → content가 남는 높이를 모두 차지하므로 `tab-bar`가 자동으로 맨 아래로 밀려남

---

#### 2. 레이어 구조 예시 (Home 화면)

```
home
├── status-bar
├── content                (H: Fill container)
│   ├── section/greeting
│   ├── section/search
│   └── section/section-title
├── tab-bar                (options)
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

##### Product Designer의 업무 프로세스
1. **문제 정의 (반복)**
   - 가설 수립 → 실제 사용자 인터뷰로 검증 → 문제 정의 수정
   - 일상에서 사람들이 겪지만 흔히 간과되는 문제를 발견하는 것이 핵심
2. **디자인**
3. **검증 (Validation)**
   - 사용성 테스트(Usability testing) 등
4. **협업 (Collaboration)**
   - PM, SWE, DA, DS 등과 함께 진행

##### 필요 역량
- **Business acumen**: 비즈니스가 어떻게 돌아가는지, 회사가 무엇을 달성하려는지에 대한 감각
- 사용자의 일상 속 니즈를 파악하는 관찰력
- 가설 검증을 비즈니스 임팩트 관점에서 판단하는 능력

##### 예시: 토스's 조직 구조
- 제품 영역별(카드, 증권, 송금, 페이 등)로 한 팀을 구성
- 각 팀에 **PM, PD, SWE, DA** 등이 모두 포함되어 해당 영역을 end-to-end로 담당
