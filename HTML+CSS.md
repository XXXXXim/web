# Structure of HTML

### HTML 구조

> `<!DOCTYPE html>`
>> 해당문서가 html 문서라는 것을 나타냄

> `<html></html>`
>> 전체 페이지의 콘텐츠를 포함

> `<title></title>`
>> 브라우저 탭 및 즐겨찾기 시 표시되는 제목으로 사용

> `<head></head>`
>> HTML문서에 관련된 설명, 설정 등 컴퓨터가 식별하는 메타데이터 작성
>> 사용자에게 보이지 않음

> `<body></body>`
>> HTML 문서의 내용을 나타냄
>> 페이지에 표시되는 모든  콘텐츠 작성
>> 한 문서에 하나의 body 요소만 존재

```html
<!DOCTYPE html>
<html>
<head>
  <title>제목</title>
</head>
<body>
  <h1>안녕하세요</h1>
</body>
</html>
```
***
### HTML Element(요소)

> 하나의 요소는 **여는 태그** 와 **닫는 태그** 그리고 그 안의 **내용** 으로 구성됨
> 닫는 태그는 태그 이름 앞에 슬래시가 존재함
> > 닫는태그가 없는 태그도 존재

### HTML Attributes(속성)
> 사용자가 원하는 기준에 맞도록 요소를 결정하거나 다양한 방식으로 요소의 동작을 조절하기 위한 값
> 목적
> >나타내고 싶지 않지만 추가적인 기능, 내용 담고싶을때
> >CSS에서 스타일 적용을 위해 해당요소를 선택하기 위한 값
***

# Text Structure

### HTML Text structure
>HTML의 중 목적 중 하나는 **텍스트 구조와 의미**를 제공하는 것
>예를 들어 h1 요소는 단순히 텍스트를 크게만 만드는 것이 아닌 현재 문서의 최상위 제목이라는 의미를 부여하는 것

#대표적인 텍스트럭쳐
> Heading&Paragraphs
> >h1~6, p

> Lists
> >ol, ul, li

> Emphasis&Importance
> >em, strong

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <p>My page</p>
  <a href="https://www.google.com/">Google</a>
  <!-- <img src="이미지 경로" alt="대체 텍스트(이미지 경로에 문제가 발생했을 때 출력되는 텍스트)"> -->
  <!-- <img src="images/sample.png" alt="샘플 이미지"> -->
  <!-- <img src="https://picsum.photos/200/300" alt=""> -->

  <h1>메인 대제목</h1>
  <h2>중제목</h2>
  <p>안녕 <strong>하세요</strong> <em>김준호</em>입니다.</p>
  <p>반갑습니다. <b>누구누구</b>입니다.</p>
  <ol>
    <li>파이썬</li>
    <li>알고리즘</li>
    <li>웹</li>
  </ol>
  <ul>
    <li>파이썬</li>
    <li>알고리즘</li>
    <li>웹</li>
  </ul>
</body>
</html>
```
***
# CSS
웹사이트 디자인

### CSS 적용방법
1. 인라인 스타일
>HTML 요소 안에 style 속성 값으로 작성

2. 내부 스타일 시트
>head태그 안에 style태그 작성

3. 외부 스타일 시트
>별도 CSS파일 생성 후 HTML **link태그**를 사용해 불러오기

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
/*externer style*/
  <link rel="stylesheet" href="style.css">
/*interner style*/
  <style>
    h2 {
      color: red;
    }
  </style>
</head>

<body>
/*inline style*/
  <h1 style="color: blue; background-color: yellow;">Inline Style</h1> 
  <h2>Internal Style</h2>
  <h3>External Style</h3>
</body>

</html>
```
***
# CSS 구문 및 선택자
### CSS구문

>선택자(Selector)
>> 누구를 꾸밀지 지정하는 부분

>선언(Declaration)
>> 어떻게 꾸밀지에 대한 구체적인 한줄명령
>> 속성과 값이 한쌍으로 이루어지며, 세미콜론으로 끝남

>속성(Property)
>> 바구고 싶은 스타일의 종류 나타냄

>값(Value)
>> 속성에 적용할 구체적인 설정을 나타냄

### CSS Selectors 종류
>기본선택자
>> 전체(*) 선택자
>>> HTML 전체 요소 선택

>> 요소(tag) 선택자
>>> 지칭한 모든 태그 선택

>> 클래스(class) 선택자
>>> 주어진 클래스 속성을 가진 모든 요소 선택

>> 아이디(id) 선택자
>>> 주어진 아이디 속성을 가진 요소 선택
>>> 문서에는 주오진 아이디를 가진 요소가 하나만 있어야 함

>> 속성([]) 선택자 
>>> 주어진 속성이나 속성값 가진 모든 요소 선택
>>> 속성의 존재여부, 값의 일치/포함 등 다양한 조건으로 요소를 정교하게 선택 가능

>결합자
>> 자손결합자
>>>첫 번째 요소의 자손요소들 선택
>>>ex) p span은 <p>안에 있는 모든 `<span>` 선택(하위레벨상관x)

>> 자식결합자
>>>첫 번째 요소의 직계 자식만 선택
>>>ex) ul>li은 `<ul>`안에 있는 모든 `<li>`선택(한 단계 아래 자식만)

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    /* 전체 선택자 */
    * {
      color: red;
    }
    /* 요소 선택자 */
    h2 {
      color: orange;
    }

    h3,
    h4 {
      color: blue;
    }

    /* class 선택자 */
    .green {
      color: green;
    }

    /* id 선택자 */
    #purple {
      color: purple;
    }

    /* 자식 결합자 */
    .green > span {
      font-size: 50px;
    }

    /* 자손 결합자 */
    .green li {
      color: brown;
    }

    /* 속성 선택자 (참고) */
    [class^="y"] {
      color: yellow;
    }
  </style>
</head>

<body>
  <h1 class="green">Heading</h1>
  <h2>선택자</h2>
  <h3>연습</h3>
  <h4>반가워요</h4>
  <p id="purple">과목 목록</p>
  <ul class="green">
    <li>파이썬</li>
    <li>알고리즘</li>
    <li>웹
      <ol>
        <li>HTML</li>
        <li>CSS</li>
        <li>PYTHON</li>
      </ol>
    </li>
  </ul>
  <p class="green">Lorem, <span>ipsum</span> dolor.</p>
  <p class="yellow">TEST</p>
</body>

</html>
```

***
# 명시도
결과적으로 요소에 적용할 CSS선언을 결정하기 위한 알고리즘

### 명시도가 높은 순
1. Inportance
2. Inline 스타일
3. 선택자(id>class>요소)
4. 소스 코드 선언 순서

# 선언: 값과 단위

### CSS Declaration
> 선택된 요소에 적용할 스타일을 구체적으로 명시하는 부분
> >목적
> >>- 선택자는 '어떤요소에' 스타일을 적용할지 결정하는 규칙이었고
> >>- 선택자로 요소를 선택했으니, 이제 중괄호 안에 '무엇을' 할지 정의
> >>- 이 '무엇을' 에 해당하는 부분이 바로 '선언'

#### 속성
>- 스타일링 하고싶은 기능이나 특성을 의미
>- CSS가 미리 정의해둔 키워드를 사용해야 함
>- font-size, color, width, margin, padding 등

#### 값
>- 속성에 적용될 구체적인 설정
>- 속성이 받을 수 있는 값의 종류는 정해져 있음
>- 16px, lightgray, 100%, 10rem

### 값의 단위(절대단위,  상대단위)
> 절대단위
> > px, pt, cm

> 상대단위
> > %, em, rem, vw, vh

#### 절대단위 대표 'px'

#### 상대단위 'em'
> - 부모 요소의 font-size를 기준으로 크기가 결정되는 상대단위
> - 만약 부모요소에 font-size가 없다면, 그 상위 부모의 font-size를 상속 받음.
> - 중첩문제가 있음(rem으로 해결), 부모요소 커지면 따라커져서 고정적이지 못함

#### 상대단위 해결사 'rem'
> - "Root em"
> - em의 단점 극복
> - 부모 요소가 아닌, 최상위요소인 `<html>`의 font-size기준으로 크기가 결정
> - html의 기본 font-size는 대부분의 브라우저에서 16px

#### rem 필요이유
1. 상속의 복잡성 해결
2. 유지보수 용이성
3. 접근성 향상
   
```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    /* rem의 기준이 되는 최상위 요소(root)의 글자 크기(브라우저 기본 글자 크기)는 보통 16px입니다. */

    /* em의 기준이 될 부모 요소 */
    .parent-for-em {
      font-size: 20px;
      border: 2px solid blue;
      padding: 10px;
      margin-bottom: 20px;
    }

    /* em 단위 사용 */
    .em-unit {
      /* 부모(.parent-for-em)의 font-size인 20px을 기준으로 1.5배 크기를 가집니다.
      계산: 20px * 1.5 = 30px
    */
      font-size: 1.5em;
    }

    /* rem 단위 사용 */
    .rem-unit {
      /* 최상위 요소(html)의 font-size인 16px을 기준으로 1.5배 크기를 가집니다.
      계산: 16px * 1.5 = 24px
    */
      font-size: 1.5rem;
      border: 2px solid red;
      padding: 10px;
    }
  </style>
</head>

<body>

  <div class="parent-for-em">
    부모 요소 (font-size: 20px)
    <div class="em-unit">
      em 단위 자식 (font-size: 1.5em ==> 30px)
    </div>
  </div>

  <div class="rem-unit">
    rem 단위 요소 (font-size: 1.5rem ==> 24px)
  </div>

</body>

</html>
```
***
# 상속
### CSS상속
>- 기본적으로 CSS는 상속을 통해 부모 요소의 속성을 자식에게 상속해 재사용성을 높임
>- 상속되는 속성
>> Text관련 요소(font, color, text-align), opacity, visibility 등

>- 상속되지 않는 속성
>> - Box model 관련 요소(width, height, border, box-sizing)
>> - position 관련 요소(position, top/right/bottom/left, z-index) 등

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .parent {
      /* 상속 O */
      color: red;

      /* 상속 X */
      border: 1px solid black;
    }
  </style>
</head>

<body>
  <ul class="parent">
    <li class="child">Hello</li>
    <li class="child">Bye</li>
  </ul>
</body>

</html>
```
