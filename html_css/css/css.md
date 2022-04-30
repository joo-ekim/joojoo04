# CSS

## 학습내용

- Contents Styling

  - Text Styling
  - Media Contents Styling => 크기, 여백

- Structure Styling => Layout

## CSS Introduction

- Cascading Style Sheet : HTML Contents를 스타일링하는 언어
- 위-아래 실행 흐름에 맞춰서 하단에 적용한 스타일이 최종 적용되어 화면에 표시

## CSS Syntax

```
selector{property:value;}
```

## CSS 작성 방법

- External : 외부 파일
- Internal : 내부 추가 태그 방식
- Inline : 내부 줄단위 방식, js에서 사용하는 방식

## id, class

- id, class attribute를 사용해서 HTML 요소에 이름을 지정

```
<p id="para1">단락내용1</p>

<p class="para2">단락내용2</p>
```

- id

  - 동일한 HTML 파일에서 단 한번만 사용되어야 함
    => 고유하게 사용됨, BackEnd 개발과 연결해서 활용
  - 동일한 HTML Element에 여러개의 id 이름을 사용할 수 없음

- class

  - 동일한 HTML 파일에서 같은 이름을 여러번 사용할 수 있음
    => 여러 요소에 스타일을 공동적용 시킬 때 활용
  - 동일한 HTML Element에 여러개의 class 이름을 사용할 수 있음
    => 스타일을 분리해서 조립하는 형태로 활용

- FE에서는 주로 class를 활용

## CSS Selector

- Simple Selector
- Element Selector
- class Selector

CSS에서 id, class를 표현하는 방법

- id => #
- class => .

```
#para1{} (id)
.para2{} (class)
```

## CSS Color

- RGB 모드 색 표현 값

  - 10진수
    - rgb() : rgb 함수
    - rgb(255,255,255) : rgb() 함수에 각각 r,g,b, 숫자 값을 대입
  - 16진수
    - 0~9, A,B,C,D,E,F (16가지 a부터 10으로 침)
    - R, G, B 각각 2자리로 표현
      -#A5F645 : 16진수 숫자값으로 표현

- 투명도
  - Opacity(불투명)
    - css property => HTML Element 자체가 투명해짐(태그 안의 모든 요소들이 투명해짐)
    - 0~1 사이의 소수점 값을 사용
  - Transparent(투명)
    - 단일 속성값
  - Alpha(알파채널)
    - 0~1 사이의 소수점 값을 사용
    - rgba() 함수 사용

```

div{
  opacity:0;
}

div{
  background-color:transparenct;
}

div{
  color:rgba(255,255,255,0.5); =>마지막 넘버는 0~1사이의 소수점 값
}
```

## CSS Text

### Text color

- color 속성

### Text Alignment

- 텍스트 정렬 : text-align
- 왼쪽(left-기본값, 가운데(center), 오른쪽(right), 양쪽정렬(justify)

### Text Decoration

- 텍스트에 줄 긋기 : text-decoration
- overline(윗줄), line turough(취소선), underline(밑줄), none(줄 없앰)

### Text Transformation

- 영문 대소문자 변경 표시

### Text Spacing

- 첫줄 들여쓰기 : text-indent
- 값 : px값

- 자간 : letter-spacing
- 값 : px값

- 단어 간격 : word-spacing
- 값: px값

- 줄 높이 : line-height
- 텍스트를 포함한 해당 줄의 높이
- 텍스트의 content-area는 텍스트와 기본여백이 포함
- 값 : px값,배수값(소수점 숫자,단위없음)

- 줄 바꿈 : white-spacing
- 값 : wrap(줄바꿈-기본값), nowrap(줄바꿈 안함)

## CSS Font

- 글꼴 종류 : font-family
  - 앞에서 부터 차례대로 설치된 폰트를 찾아서 설치되어 있는 폰트를 화면에 랜더링 함
  - Fallback 기능

```
p{
  font-family:arial, helvetica, sans-serif;
}
```

- Fallback 기능 원리

  - 브라우저가 폰트를 찾는 기본 위치 : 시용자(클라이언트) PC
  - 폰트 종류를 선택할 때 사용자들이 범용으로 사용할 만한 폰트를 선택 => Web safe font
  - 웹 안전 폰트 : 돋움, 굴림

- 브라우저가 폰트를 서버에서 찾도록 하는 기능 => Web font

  - 로컬 서버에 직접 웹폰트 파일을 업로드해서 사용
  - 웹 폰트 서비스를 사용 - 구글 폰트

- 글꼴 기울임 : font-style
- 값 : italic

- 글꼴 굵기 : font-weight
- 값 : bold/nomal, 숫자값

- 글꼴 크기 : font-size
- 값 : px값

### Web Font

- 로컬 서버에 웹 폰트 파일을 업로드해서 사용하는 방법
  - local() 함수 : 사용자 pc에 설치된 폰트 검색
  - url() 함수 : 웹 폰트 파일 불러오기
  - format() 함수 : 브라우저에서 지원하는 파일만 다운로드
  - 한글 : 본고딕(Noto Sans), 나눔바른고딕
  - 영문 : roboto, lato, open sans, montserrat
  - 고딕체 : sans-serif
  - 명조체 : serif

```
  @font-face{
        font-family:"NB-regular";
        src:local(nanumbarun),
            url(/resources/nbg_r.woff) format("woff");
        font-style:normal;
        font-weight:normal;

  }
```

## CSS link

- 4가지 상태 구분
- link, visited, hover, active

## CSS 상속, cascading, 우선 순위

- 상속

  - 포함 관계의 HTML 구조에서 부모요소에 적용한 CSS 속성이 자식요소에도 적용되는 것
  - 모든 CSS 속성이 상속되는 것은 아님

- cascading, 우선 순위
  - cascading : 나중에 적용한 CSS가 최종 적용되어 표시
  - 우선순위 : 선택자의 우선 순위에 따라서 적용되는 순서를 변경할 수 있음
    - id : 100점
    - class : 10점
    - tag : 1점

## 네이밍 표기법 : naming()intro => 두개 이상의 단어로 네이밍을 할 때, 단어 사이의 구분을 하는 방법

- naming-intro : kebab case => id, class, url 경로
- naming_intro : snake case => file, folder
- namingIntro : camel case (첫번째는 소문자, 이어붙여서 두번째 단어는 대문자) => js의 변수, 함수 이름
- NamingIntro : pascal case (첫번째, 두번째 모두 대문자) => js Class 이름

## Box model

### Height / Wigth

- 박스 크기 지정

- px : 지정된 값으로 고정
- %
  - width : 부모요소를 기준으로 값 비율만큼 지정
  - height : 자식요소를 기준으로 맞춰짐 => % 지정이 적용되지 않음

### Padding

- 방향별 개별 적용
  - padding-top
  - padding-right
  - padding-bottom
  - padding-left

- padding : 축약 표현
  - 값 4개
  - 값 3개
  - 값 2개
  - 값 1개

** top에만 padding을 적용하는 경우

```
div{
  padding-top:100px;
}

div{
  padding:100px 0 0 0;
} => 0은 px 표시를 하지 않는다
```

### margin

- padding과 사용방법이 같음

- auto : 왼쪽, 오른쪽 여백이 동일하게 적용 => 박스 가운데 배치



