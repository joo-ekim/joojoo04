# HTML

## 학습 내용

- Contents
  - Text Contents
  - Image, Video, Audio Contents
- Structure

## HTML Introduction

- Hyper Text Markup Language
- HTML을 사용해서 웹페이지에 콘텐츠와 구조를 표시

## HTML Basic

```
<!DOCTYPE html> : 문서(웹페이지) 타입(종류) - 버전(HTML5)
<html> : 웹 페이지 전체 영역

  <head> : 웹 페이지의 추가정보, 타이틀, 파일 임포트
      <title></title>
  </head>

  <body> : 웹 페이지의 본문 영역 - 웹 페이지 모든 콘텐츠 표시
  </body>

</html>
```

## HTML Syntax

- Tag를 사용해서 Element를 표시/표현

```
<tag>cintents</tag> : 시작태그, 종료태그로 구성

<tag> : 시작 태그만 존재하는 경우 - 빈요소(Empty Element)
```

- 포함관계(Nested Element)
  - Tag 영역안에 다른 Tag가 포함되는 것
  - 포함하는 요소 : 조상요소(ancestor), 부모요소(parent)
  - 포함되는 요소 : 자손요소(descendant), 자식요소(child)

```
<html>
  <body>
    <h1>큰제목</h1>
    <p>단락</p>
  </body>
</html>

html 기준
- 자식요소 : body
- 자손요소 : h1, p
body 기준
- 조상요소 : X
- 부모요소 : html
- 자식요소 : h1, p
- 자손요소 : X

```

- Attribute(속성)
  - tag에 추가 정보
  - attr이름 = "값"

```
  <tag attr="값"></tag>
```

## Text Contents Markup

### Heading(제목)

- h(eading) 태그
- h1 ~ h6

### Paragraph(단락)

- p (aragraph) 태그

```
WYSIWYG(What You See Is What You Get : 네가 보는것이 얻는 것이다)
- HTML은 WYSIYG 지원이 되지 않음
```

- 강제 줄바꿈 : br(eak) 태그

  - 시작태그만 존재하는 빈요소(Empty Element)

- 강제 공백 : &nbsp;(Non-Break Space)(엔터티 코드)

```
 - & : ampersand

 엔터티코드 : 대체코드
  - 특수문자를 직업 사용하지 못할때 대체해서 사용하는 코드
```

- 수평선(Horizontal Rule) : hr
  - 단락을 구분하는 구분선
  - 빈 요소

### HTML Link

- a(nchor) : 하이퍼링크 연결 태그
- href(hypertext reference) : 목적지 정보 제공 속성(attribute)
- bookmark
  - 연결된 페이지로 이동하지 않고, 같은 페이지 내에서 위아래 이동

```
-  pase Link
<a href="url">텍스트</a>

- bookmark

- Link
< a href="#targer">목적지</a>

- target
<h2 id="target">단락 제목</h2>
```

- url(Uniform Resource Locator) : 파일(자원)위치식별자 - 상세주소
  바뀌지 않는 자원(고정된 자원 ->파일) 위치식별자 / 파일위치식별자
- 인터넷 주소체계
  - IP(Internet Protocol) adress
  - Domain name : IP 주소를 영어단어로 표현
    - 서버종류 : www
    - 회사이름 : navver, daum
    - 기관성격 : com, net (3자리) / co, go, ac (4자리)
    - 국가(4자리) : kr, uk, ca, fr ...

```
- IP : 0~255까지 숫자 4개로 구성
ex) 192.168.0.1

- 인터넷 접속 프로세스 : 주소표시줄에 Domain Name 입력 => IP주소로 변환 => 접속

- URL 체계

IP또는 Domain 주소/상세경로/파일정보
ex)www.w3schools.com(주소)/html(상세경로)/defauit.asp(파일정보)

```

### HTML Table

```
<table> : 테이블 작성
  <tr> : table row - 행
    <th></th> : table header - 열제목(맨 위에 한번만 사용됨)
  </tr>
  <tr>
    <td></td> : table data - 데이터
  </tr>
</table>
```

### HTML List

- ul(Unordered List) : 순서없는 목록
  - 기호로 표시
- ol(ordered List) : 순서있는 목록
  - 숫자로 표시(알파벳,한글)
- li(List Item) : 목록 아이템

```
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JS</li>
</ul>

<ol>
  <ol>HTML</ol>
  <ol>CSS</ol>
  <ol>JS</ol>
</ol>


```

- Description List : 설명목록
  - dl (Description List)
  - dt (Description title)
  - dd (Description Data)
  ```
  <dl>
    <dt>목록 주제</dt>
    <dd>목록 설명</dd>
  </dl>
  ```
