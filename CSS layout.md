# CSS Box
- CSS Box Model
  > 웹 페이지의 모든 HTML 요소를 감싸는 사각형 상자 모델
## 박스 구성 요소
- Margin
  > 이 박스와 다른 요소와의 외부 간격
- Border
  >content와 padding을 감싸는 테두리
- padding
  > content와 border 사이의 내부 여백
- content
  > 실제 내용이 위치하는 영역

# shorthand 속성(단축속성)
### shorhand 속성: 'border'
- border-width, border-style, border-color를 한번에 설정하기 위한 속성
  > 작성순서는 영향 X
  ``` html
    border: 2px soild black;
  ```

### shorthand 속성: 'margin' & 'padding'
- 4방향의 속성을 각각 지정하지 않고 한번에 지정할 수 있는 속성
- <img width="360" height="301" alt="image" src="https://github.com/user-attachments/assets/d2eb097e-5990-4cf2-b6d4-9caa35efa2da" />

# box-sizing 속성 (박스의 크기 계산법)

### The standard CSS box model
> 1. 표준 상자 모델에서 width와 height 속성 값을 설정하면, 이 값은 content box 의 크기를 조정하게 됨
> 2. CSS는 border box가 아닌 content box의 크기를 width값으로 지정
<img width="808" height="278" alt="image" src="https://github.com/user-attachments/assets/4adf2f44-a985-4b20-b3d9-25bd8913f5ef" />

## The alternative CSS box model
- 대체 상자 모델에서 모든 width와 height는 실제 상자의 너비
- 실제 박스 크기를 정하기 위해 테두리와 패딩을 조정할 필요 없음
- <img width="393" height="202" alt="image" src="https://github.com/user-attachments/assets/44e9f0d1-67f5-4c39-8a40-2050447475e4" />

<img width="780" height="387" alt="image" src="https://github.com/user-attachments/assets/350f3ff4-a894-490d-ae79-e20046acfea6" />
<img width="888" height="380" alt="image" src="https://github.com/user-attachments/assets/97e9f2a4-fac5-4a30-b199-8da0ac1b0af5" />

***
# display속성 (박스의 화면 배치 방식)
## 박스타입
1. Block 타입
2. Inline 타입

### block타입
<img width="469" height="120" alt="image" src="https://github.com/user-attachments/assets/d04dedcf-7f53-4e69-92d4-a21b6ce26a29" />

- 하나의 독립된 덩어리처럼 동작하는 요소
  ```html
  .index{
  display: block;
  }
  ```

- 항상 새로운 행으로 나뉨(한 줄 전체를 차지, 너비100%)
- width, height, margin, padding 속성을 모두 사용 가능
- padding, margin, border로 인해 다른 요소를 상자로부터 밀어냄
- width 속성을 지정하지 않으면 박스는 inline 방향으로 사용 가능한 공간을 모두 차지함
  > 상위 컨테이너 너비 100%로 채우는 것
- 대표적인 block 타입 태그
  >h1~6, p, div, ul, li

### block 타입 대표: div
- 다른 HTML요소들을 그룹화하여 레이아웃을 구성하거나 스타일링을 적용할 수 있음
- 헤더, 푸터, 사이드바 등 웹 페이지의 다양한 섹션을 구조화 하는 데 가장 많이 쓰이는 요소
  <img width="600" height="272" alt="image" src="https://github.com/user-attachments/assets/82426b8d-df45-4fb7-b3c3-f0f9772556cc" />

### Inline 타입
<img width="457" height="99" alt="image" src="https://github.com/user-attachments/assets/f390cfb8-c9b2-4af0-97e6-9329b11c4eb4" />

- 문장안의 단어처럼 흐름에 따라 자연스럽게 배치되는 요소
  ```html
  .index{
  display: inline;
  }
  ```

- 줄 바꿈이 일어나지 않음(콘텐츠의 크기만큼만 영역을 차지)
- width 와 height 속성을 사용할 수 없음
- 수직방향(상하)
  >padding, margin, border가 적용되지만, 다른 요소를 밀어낼 수 는 없음'
- 수평방향(좌우
  >padding, margin, border가 적용되어 다른 요소를 밀어낼 수 있음
- 대표적인 inline 타입 태그
  > a, img, span, strong

### Inline 타입의 대표: span
- 자체적으로 시각적 변화 없음
  >스타일을 적용하기 전까지는 특별한 변화 없음
- 텍스트 일부 조작
  >문장 내 특정 단어나 구문에만 스타일을 적용할 때 유용
- 블록요소처럼 줄바꿈을 일으키지 않으므로 문서의 구조에 큰 영향을 주지 않음
  <img width="830" height="227" alt="image" src="https://github.com/user-attachments/assets/9e025743-a471-44ab-80f9-3f1e064eac1f" />

# Normal flow
- 일반적인 흐름 또는 레이아웃을 변경하지 않는 경우 웹 페이지 요소가 배치되는 방식
  <img width="609" height="81" alt="image" src="https://github.com/user-attachments/assets/838cdddb-7237-43e5-a8ef-38e5c64cbaa3" />
  <img width="897" height="433" alt="image" src="https://github.com/user-attachments/assets/9ee939fb-fdea-4bf1-a24a-725ee6dad49e" />

# 기타 display 속성
1. inline-block
2. none
3. flex

### inline-block 타입
- inline과 block의 특징을 모두 가진 특별한 display 속성 값
  <img width="466" height="83" alt="image" src="https://github.com/user-attachments/assets/f69960b3-2c38-4b7b-ad61-a7300357d81c" />
  ```html
  .index{
  display: inline-block;
  }

- block과 inline의 특징을 합친 것(줄 바꿈 없이, 크기 지정 가능)
- width 및 height 속성 사용 가능
- padding, margin 및 border로 인해 다른 요소가 상자에서 밀려남
- ex) 가로로 정렬된 내비게이션 메뉴나 여러개의 버튼, 이미지 갤러리 처럼 수평으로 나열하면서 각 항목의 크기를 직접 제어하고 싶을때
  <img width="865" height="442" alt="image" src="https://github.com/user-attachments/assets/ea21bfd8-0715-46e9-b829-2c3c46fd57ed" />

### none 타입
- 요소를 화면에 표시하지 않고, 공간조차 부여하지 않음
  <img width="469" height="131" alt="image" src="https://github.com/user-attachments/assets/14af6179-7275-49c1-95b6-c2a950cb72e3" />
  ```html
  .index {
  display: none;
  }
  ```
  <img width="891" height="410" alt="image" src="https://github.com/user-attachments/assets/8cb10d67-aaa3-45ca-af1d-4c15c34ec9ad" />


