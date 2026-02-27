# Responsive Web

## 반응형 웹 디자인
- 디바이스 종류나 화면 크기에 상관없이 어디서든 일관된 레이아웃 및 사용자 경험을 제공하는 디자인 기술

## UX(user experience)
- 제품이나 서비스를 사용하는 사람들이 느끼는 전체적인 경험과 만족도를 개선하고 최적화하기 위한 디자인과 개발분야

> > **감각적경험(브랜드인식**
> > >러쉬 매장 근처만 가도 느껴지는 특유의 향기 등

>>**기능적 경험(사용성)**
> > >음악 앱 검색창에 오타를 입력해도 찰떡같이 찾아주는 스마트한 검색결과

> > **편의적 경험(흐름)**
> > >바쁜 아침, 모바일 오더를 통해 줄 서는 과정 없이 매장에 도착하자 마자 커피를 픽업하는 매끄러운 경험

#### UX설계
-사용자의 숨겨진 니즈와 행동 패턴을 데이터를 통해 깊이 이해하고, 이를 바탕으로 제품의 구조와 사용 흐름을 논리적으로 구체화하는 과정
> 이해 및 분석, 구조화, 구체화 및 검증

## UI(user interface)
- 서비스와 사용자 간의 상호작용을 가능하게 하는 디자인 요소들을 개발하고 구현하는 분야

- **물리적UI(hardware):리모컨**
>단순히 버튼을 누르는 동작을 넘어, 자주 쓰는 버튼(전원,볼륨)의 크기와 위치, 그립감, 버튼 눌림감 등 물리적인 조작 인터페이스

- **복합적 UI(Hybrid): ATM기기**
>화면 속 터치버튼 크기와 배치 뿐 아니라 투입구 깜빡임 비밀번호 물리 키패드 가림막 등

- **디지털UI(software): 웹/앱 로그인 화면**
>사용자가 헤매지 않도록 입력창 명확히 배치, 생상과 위치 경고문구 등 시각적 요소의 총체

### UI 설계
- 단순히 보기좋은 디자인을 넘어 정보의 위계를 잡앗 ㅏ용자가 무엇을 먼저 봐야할지 유도, 일관성을 통해 학습 비용을 줄이는 것
>레이아웃&그리드, 타이포그래피&컬러, 인터랙션 요소
>>와이어프레임, 디자인시스템, 프로토타입 <<<필요 도구 및 산출물
***
# Bootstrap Grid System
- 웹 페이지의 레이아웃을 조정하는 데 사용되는 **12개 컬럼** 으로 구성된 시스템

### 12컬럼의 마법
- 12칸 중 크기에 따라 필요한만큼의 컬럼을 차지하게 요소를 배치
> 내부의 요소도 12칸으로 나눠서 활용
<img width="914" height="313" alt="image" src="https://github.com/user-attachments/assets/1a9a166d-984f-4fb4-9bd0-acf66cbf7433" />

# Grid system 구조와 문법
### Grid system 기본요소
- Container
 column들을 담고있는 결과
<img width="918" height="222" alt="image" src="https://github.com/user-attachments/assets/56e750ad-fed3-49dc-8b20-9a455028245d" />

- Column
실제 컨텐츠를 포함하는 부분
<img width="913" height="223" alt="image" src="https://github.com/user-attachments/assets/150de55d-d11a-4694-ac90-7534fd918d0e" />

- Gutter
컬럼과 컬럼사이 여백영역(상하좌우)
<img width="918" height="200" alt="image" src="https://github.com/user-attachments/assets/6b33ae72-da1b-4795-b26d-4a141ba6fa31" />

- 1개의 row 안에 12개의 column 영역이 구서
 - 각 요소는 12개 중 몇 개를 차지할 것인지 지정됨
<img width="902" height="219" alt="image" src="https://github.com/user-attachments/assets/54913896-0e94-43ec-9fda-ea4997f3cdb7" />


***
# 추가학습 
1. Basic (Container, Row, Column)
- 부트스트랩 그리드의 절대 법칙: "**모든 가로줄(Row)은 12칸**의 피자 조각으로 나뉜다."

- container: 피자를 담는 튼튼한 '박스'야. 양옆에 적당한 여백을 줘서 내용물이 예쁘게 가운데로 오게 해줘.

- row: 피자를 가로로 자르는 '선'이야. 반드시 container 안에서 써야 해.

- col-*: "나는 12조각 중에서 몇 조각을 먹을래!" 하고 선언하는 거야.

__[구현 코드: Basic의 빈칸 채우기]__
두 번째, 세 번째 줄의 빈칸에 알맞은 조각 수를 넣어줘야 해. 합쳐서 12가 되도록!
```html
HTML
    <div class="row">
      <div class="col-4">
        <div class="box">col-4</div>
      </div>
      <div class="col-4">
        <div class="box">col-4</div>
      </div>
      <div class="col-4">
        <div class="box">col-4</div>
      </div>
    </div>
    <div class="row">
      <div class="col-2">
        <div class="box">col-2</div>
      </div>
      <div class="col-8">
        <div class="box">col-8</div>
      </div>
      <div class="col-2">
        <div class="box">col-2</div>
      </div>
    </div>
```
2. Nesting (중첩)
Nesting은 **"피자 조각 안에 또 다른 12조각짜리 미니 피자를 만드는 것"**이야.

>네 코드를 보면 `<div class="col-8 box">` 안에 또 `<div class="row">`가 들어있지?
- 이게 핵심이야. 부모가 col-8이든 col-4든 상관없이, 새로운 row가 시작되면 그 안은 무조건 다시 '12칸'으로 리셋돼. 그래서 그 안에 col-6 4개가 들어갈 수 있는 거야. (단, 6+6=12 니까 2개씩 두 줄로 알아서 줄바꿈이 되겠지!)

3. Offset (건너뛰기)
- Offset은 **"투명 망토를 입은 유령 칸"**을 만드는 기능이야. 박스를 오른쪽으로 밀어버리고 싶을 때 써.

- offset-4: "내 왼쪽에 4칸짜리 투명한 공간을 만들어 줘!" 라는 뜻.

__[구현 코드: Offset의 빈칸 채우기]__
- 마지막 빈칸을 보면 col-6 offset-3이라고 적혀있지? 이걸 클래스에 쏙 넣어주면, 왼쪽에서 3칸을 띄우고 자기는 6칸을 차지하니까 **완벽한 정중앙 배치(3+6+3=12)**가 돼.
```html
HTML
    <div class="row">
      <div class="col-6 offset-3">
        <div class="box">col-6 offset-3</div>
      </div>
    </div>
```
4. Gutters (여백)
- Gutter는 **"기둥(Column)과 기둥 사이의 틈(간격)"**이야. 박스들이 너무 다닥다닥 붙어있으면 답답하니까 숨통을 트여주는 거지. row 태그 옆에 붙여서 사용해.
>>x축은 padding, y축은 margin으로 여백 생성

- gx-*: X축(가로) 간격

- gy-*: Y축(세로) 간격

- g-*: X, Y축(사방) 동시 간격

- 숫자는 0부터 5까지 쓸 수 있어. (gx-0은 틈을 완전히 없애버리겠다는 뜻!)

__[구현 코드: Gutters의 텅 빈 뼈대 채우기]__
- Y축 간격을 눈으로 확인하려면 줄바꿈이 일어나야 해서 col-6을 4개씩 넣었어.
```html
HTML
  <h2 class="text-center">Gutters(gx-0)</h2>
  <div class="container">
    <div class="row gx-0"> <div class="col-6"><div class="box">col</div></div>
      <div class="col-6"><div class="box">col</div></div>
    </div>
  </div>

  <hr>

  <h2 class="text-center">Gutters(gy-5)</h2>
  <div class="container">
    <div class="row gy-5"> <div class="col-6"><div class="box">col</div></div>
      <div class="col-6"><div class="box">col</div></div>
      <div class="col-6"><div class="box">col</div></div>
      <div class="col-6"><div class="box">col</div></div>
    </div>
  </div>

  <hr>

  <h2 class="text-center">Gutters(g-5)</h2>
  <div class="container">
    <div class="row g-5"> <div class="col-6"><div class="box">col</div></div>
      <div class="col-6"><div class="box">col</div></div>
      <div class="col-6"><div class="box">col</div></div>
      <div class="col-6"><div class="box">col</div></div>
    </div>
  </div>
```
***
# Grid system for responsive web
## Breakpoints
- 웹페이지를 다양한 화면 크기에서 적절하게 배치하기 위한 분기점
> 화면 너비에 따라 6개의 분기점 제공(xs, sm, md, lg, xl, xxl)
- 각 breakpoints 마다 설정된 최대 너비 값 **이상으로** 화면이 커지면 grid system 동작이 변경됨
***

# 레이아웃, 무엇을 언제 쓸까
- Position
> 벽에 붙인 스티커, 혹은 포스트잇
> >흐름을 무시하고 원하는 좌표에 콕 집어 배치(겹침) 할 때

-Flexbox
>방 안의 가구
>>Grid로 나눈 구역 내부(디테일)를 정렬할 때

- Bootstrap Grid System
>건물의 뼈대
>>웹 페이지의 전체적인 구조(큰 틀) 잡을때

### " 숲(전체)은 Bootstrap Grid system으로 빠르게짓고, 나무(디테일)는 Flexbox로 섬세하게 다듬기"

# Grid cards
- row-cols 클래스를 사용하여 행당 표시할 열(column) 수를 손쉽게 제어할 수 있음.
```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-sRIl4kxILFvY47J16cr9ZwB07vP4J8+LH7qKQnuqkuIAvNWLzeN8tE5YBujZqJLB" crossorigin="anonymous">
</head>

<body>
  <h2 class="text-center">Grid Cards</h2>
  <div class="container">
    <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 g-4">
      <div class="col">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
              content. This content is a little bit longer.</p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
              content. This content is a little bit longer.</p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
              content.</p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Card title</h5>
            <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional
              content. This content is a little bit longer.</p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-FKyoEForCGlyvwx9Hj09JcYn3nv7wiPVlz7YYwJrWVcXK/BmnVDxM+D2scQbITxI"
    crossorigin="anonymous"></script>
</body>

</html>
```
