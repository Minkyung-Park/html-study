# 2. 스타일

## 2.1 스타일 시트

- 브라우저 기본 스타일
  - 웹 브라우저에서 기본으로 사용하는 스타일
- 인라인 스타일
  - style 속성을 사용해서 필요한 요소에 스타일 직접 지정
- 내부 스타일 시트
  - 문서 앞 부분에 스타일을 모아서 함께 정리하고 관리
- 외부 스타일 시트
  - 스타일을 따로 파일로 저장한 후 연결

## 2.2 CSS 기본 선택자(Selector)

1. 전체 선택자(\*)

- 문서 모든 요소에 스타일을 적용
- \* {margin: 0 auto;}

2. 타입 선택자

- 특정 태그를 사용한 모든 요소에서 스타일 적용
- p {font-style: italic;}

3. 클래스 선택

- 특정 부분만 선택해서 문서 안에 여러번 적용
- .bg {background-color: #fff;}

4. 그룹 선택자

- 여러 요소에 같은 스타일을 적용
- h1, h2, h3 {text-align: center;}

5. id 선택자

- #id{}

## 2.3 스타일 우선순위

1. 얼마나 중요한가?

- 사용자 스타일 -> 제작자 스타일 -> 브라우저 기본 스타일

2. 적용 범위 어디까지인가?

- !important -> 인라인 스타일 -> id 스타일 -> class 스타일 -> 타입 스타일

3. 소스 작성 순서

- 나중에 작성한 스타일이 먼저 작성한 스타일을 덮어쓴다.

# 텍스트 스타일

## 3.1 글자와 관련된 속성

- font-family : 글꼴 종류 지정
- font-size : 글자 크기 지정
- font-style : 글자 italic으로 표시할지 지정
- font-weight : 글자의 굵기 지정

## 3.2 텍스트 스타일 속성

- color : 글자색 지정
- text-decoration : 텍스트에 밑줄, 취소선 표시할지 여부
- text-transform : 텍스트 전체 또는 첫 글자를 대문자로 표시할지 여부
- text-shadow : 텍스트에 그림자 추가
- letter-spacing : 글자 사이의 간격(자간)
- word-spacing : 단어 사이의 간격
- text-align : 텍스트 정렬방법 지정
- lign-height : 줄 간격 조절(행간)

## 3.3 웹에서 색상을 지정하는 방법

- 16진수 Hex : #000
- rgb, rgba : rgba(255, 255, 255, 0.7)
- hsl, hsla
- 색상 이름 white, black

## 3.4 텍스트를 정렬하는 text-align 속성

- start : 현재 텍스트 줄의 시작 위치에 맞추어 문단을 정렬
- end : 현재 텍스트 줄의 끝 위치에 맞추어 문단을 정렬
- left : 왼쪽 맞춤
- right : 오른쪽 맞춤
- center : 가운데 맞춤
- justify : 양쪽 맞춤
- match-parent : 부모 요소를 따라 문단 정렬

## 3.5 줄 간격을 조절하는 line-height 속성

- 보통 1.25 ~ 1.75배 정도 추천

## 3.6 텍스트의 줄을 표시하거나 없애 주는 text-decoration 속성

- 텍스트에 밑줄을 긋거나 취소선을 표시
- 하이퍼링크 밑줄 없애기 등에 사용
- none
- underline
- overline
- line-through

## 3.7 텍스트에 그림자 효과 text-shadow 속성

- text-shadow: 가로거리 세로거리 번짐정도 색상

## 3.8 텍스트의 대소문자를 변환하는 text-transform 속성

- 영문자
- capitalize : 첫 번째 글자를 대문자로
- uppecase : 모든 글자를 대문자
- lowercase : 모든 글자를 소문자
- full-width : 가능한 모든 문자를 전각 문자로 변환

## 3.9 글자 간격을 조절하는 letter-spacing, word-spacing

- letter-spacing : 자각
- word-spacing : 단어와 단어 사이의 간격을 조절

## 3.10 목록 스타일

### 3.10.1 bullet 모양과 번호 스타일을 지정하는 list-style-type 속성

- disc : 채운 원모양
- circle : 빈 원 모양
- square : 채운 사각형
- decimal : 1부터 시작하는 10진수
- decimal-leading-zero : 앞에 0이 붙는 10진수(01, 02, 03)
- lower-roman : 로마 숫자 소문자
- upper-roman : 로마 숫자 대문자
- lower-alpha or lower-latin : 알파벳 소문자
- upper-alpha or upper-latin : 알파벳 대문자
- none : bullet이나 숫자를 없앤다.

### 3.10.2 bullet 대신에 이미지를 사용하는 list-style-image 속성

```css
ul {
  list-style-image: url("image.png");
}
```

### 3.10.3 목록을 들여쓰는 list-style-position 속성

- inside
- outside

```html
<ul style="list-style-position: inside"></ul>
```

### 3.10.4 목록 속성을 한꺼번에 표시하는 list-style

```html
ul {list-style list-style: url() none inside }
```

### 3.10.5 표 스타일

# 4. 레이아웃을 구성하는 CSS Box Model

- 웹 문서에서 내용을 배치할 때는 각 요소를 박스 형태로 구성
- 박스 모델은 실제 내용이 들어가는 콘텐스 영역, 테두리, 여백으로 구성

## 4.1 CSS와 Box Model

- 웹 문서의 내용을 박스 형태로 정의하는 방법
- 박스 모델이 모여서 웹 문서를 이룬다
- 박스 모델에는 margin, padding, 테두리 등 박스가 **여러 겹** 들어 있다

### 4.1.1 블록 레벨 요소와 인라인 레벨 요소

- block 요소 : 태그를 사용해서 요소를 삽입했을 때 혼자 **한 줄**을 차지하는 것, 해당 요소의 너비는 100%
- h1, div, p 등

- inline 요소 : 한 줄을 차지하지 않고 **컨텐츠** 만큼만 영역을 차지
- 따라서 한 줄에 인라인 요소를 여러 개 표시할 수 있다
- a, span, img, strong 등

### 4.1.2 박스 모델의 기본 구성

- Box Model은 컨텍츠 영역
- Box와 컨텍츠 영역 사이의 여백인 패딩
- Box의 테두리 그리고 여러 Box Model 사이의 여백인 마진

### 4.1.3 콘텐츠 영역의 크기를 지정하는 width, height 속성

- 단위 : px이나 em단위로 지정, 그러나 주로 px, rem 단위를 많이 씀
- em은 부모 요소의 글꼴 크기에 상대적임
- 그래서 root em인 rem 단위를 쓰는 것이 일관된 크기 조정에 용이
- 백분율 : 박스 모델을 포함하는 부모 요소를 기준으로 너비, 높이 값을 백분율(%)로 지정
- auto : 박스 모델의 너비, 높이 값이 컨텐츠 양에 따라 자동으로 결정(기본값)

### 4.1.4 박스 모델의 크기를 계산하는 box-sizing 속성

- border-box : 테두리까지 포함해서 width 값을 지정
- content-box : 컨텐츠 영역만 width 값을 지정(기본값)
- 웹 문서 레이아웃을 만들 때 요소의 크기를 쉽게 계산하려면 border-box로 지정

### 4.1.5 박스 모델에 그림자 효과를 주는 box-shasow 속성

- box-shadow : 수평거리 수직거리 흐림정도 번짐정도 색상 inset
- 수평거리 : 양수(오른쪽), 음수(왼쪽), 필수속성
- 수직거리 : 양수(아래쪽), 음수(위쪽), 필수속성
- 흐림정도 : 생략 시 0을 기본값으로 진한 그림자, 커질 수록 부드러움
- 번짐정도 : 양수(모든방향으로 퍼짐), 음수(모든방향으로 축소), 기본값 0
- 색상 : 한가지 또는 공백으로 구분하여 여러 색상 지정 가능
- inset : 그림자 안쪽으로

## 4.2 테두리 스타일 지정

### 4.2.1 박스 모델의 방향 살펴보기

- top -> right - bottom -> left 시계 방향 순서

### 4.2.2 테두리 스타일을 지정하는 border-style 속성

- none : 기본값, 테두리 없음
- hidden : 테두리 감춤
- solid : 실선
- dotted : 점선
- dashed : 짧은 직선
- double : 이중선, 두 선 사이의 간격은 border-width 값
- groove : 홈이 파인 듯 입체 느낌
- inset : 표에서 사용
- outset : 표에서 사용
- ridge : 튀어나온 듯한 입체 느낌
