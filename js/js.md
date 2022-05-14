# Javascript

- 프로그래밍 언어
  - 문법

- HTML, CSS 제어 기능
  - 활용

## Javascript 기초 개념

  - version
    - ES5
    - ES6

  - 작성방식
    - External
      - head 태그 영역 상단에 위치할 때 defer를 사용 가능
    - Internal
      - defer를 사용하지 못하기 때문에 HTML 요소보다 하단에 작성
    - Inline

## 문법(Syntax)

  - 데이터/변수/연산 =>기본타입
  - 명령문(구문)
  - 함수
  - 배열/객체/Class => 참조타입
  - 추가문법

### 데이터/변수/연산

- 데이터 타입(종류)
  - 문자
    - 따옴표로 묶어줌
    Ex) 'Volvo', '10'

  - 숫자
    - 정수, 실수

- 데이터 타입 구분 여부
  - 자바스크립트는 데이터타입을 구분하지 않음
  - 데이터 무결성 측면에서는 단점
  - 편리한 사용성 측면에서는 장점

- Type Script : Javascript + Data Type

```
1 + '1' = 2
```

- 변수
  - 데이터를 저장하는 공간(컨테이너)
  - 사용
    - 변수 선언
    - 변수 초기화
    - 데이터 할당

- 예약어(keyword)

```
var j; (변수선언)
j = 0; (변수 초기화)
j = 10; (데이터 할당)

var c = 20;
```

- var, let, const
  - var : ~ES5
  - let, const : ES6~

- var, let
  - 데이터 초기화 할당 이후에 변수값을 변경할 수 있음
- const
  - 데이터 초기화 할당 이후에 변수값을 변경할 수 없음