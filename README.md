## 1.2 웹 문서 구조를 만드는 시맨틱 태크

- 웹 사이트 구조는 헤더, 본문, 푸터, 사이드 바 등으로 나누어짐
- 시멘틱 태그 Can I use 사이트 참고
- main 태그 : 웹 문서에서 핵심이 되는 내용, 웹 문서마다 다르게 보여주는 내용으로 구성, 웹 문서 한 번만 사용할 수 있음
- article 태그 : 블로그의 포스트나 뉴스 사이트의 기사처럼 독립된 웹 컨텐츠 항목으로 여러개 사용 가능
- section 태그 : 웹 문서의 컨텐츠 영역을 나타냄, article은 독립된 콘텐츠, section은 몇 개의 컨텐츠를 묶는 용도
- aside 태그 : 사이드바를 만들 때, 필요한 경우에 사용
- footer 태그 : 웹 문서 맨 아래쪽에 있는 footer 영역을 만든다
  웹 사이트의 정보, 저작권 정보, 연락처 등을 넣음
- div 태그 : 영역을 나눔

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Semantic 태그</title>
  </head>
  <body>
    <!-- 헤더 영역 -->
    <header>
      <!-- 로고 영역 -->
      <div>
        <a href="#"><h1>Dream Jeju</h1></a>
      </div>
      <hr />
      <!-- 네비게이션 영역 -->
      <nav>
        <li><a href="#">단체 여행</a></li>
        <li><a href="#">맞춤 여행</a></li>
        <li><a href="#">갤러리</a></li>
        <li><a href="#">문의하기</a></li>
      </nav>
      <hr />
    </header>

    <!-- 메인 영역 -->
    <main>
      <section>
        <h2>몸과 마음이 치유되는 섬</h2>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur,
        ratione maxime. Voluptatibus nulla enim aliquam tenetur quisquam qui
        fuga voluptates, labore assumenda accusamus, possimus soluta facilis
        fugit. Perspiciatis, corporis officiis.
      </section>
      <section>
        <h2>다양한 액티비티가 기다리는 섬</h2>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur,
        ratione maxime. Voluptatibus nulla enim aliquam tenetur quisquam qui
        fuga voluptates, labore assumenda accusamus, possimus soluta facilis
        fugit. Perspiciatis, corporis officiis.
      </section>
    </main>

    <!-- 푸터 영역 -->
    <footer>
      <div>
        <ul>
          <li><a href="#">회사 소개</a></li>
          <li><a href="#">개인정보처리방침</a></li>
          <li><a href="#">여행약관</a></li>
          <li><a href="#">사이트맵</a></li>
        </ul>
      </div>
    </footer>
  </body>
</html>
```

## 1.3 웹 문서에 다양한 내용 입력하기

### 1.3.1 텍스트 입력하기

- 제목을 나타내는 h 태그
- 텍스트 단락을 만드는 p 태그, 줄바꿈 br 태그
- 인용할 때 쓰는 blockquote 태그
- 택스트를 굵게 표시 strong, b
- 기울인 텍스트를 입력해주는 em, i

### 1.3.2 목록 만들기

- 순서 있는 목록 ol, li
- 순서가 없는 몰록 ul, li
- 설명 목록을 만드는 dl, dt, dd 태그
  dl : description list
  dt : 제목
  dd : 값(설명)

### 1.3.3 표 만들기

### 1.3.4 이미지 삽입

### 1.3.5 오디오와 비디오 삽입하기

- 멀티미디어 파일을 삽일할 때쓰는 object, embed 태그
- audio, video
- a 태그 새창으로 열기 target="\_blank"

## 1.4 입력 양식 작성하기

### 1.4.1 폼 삽입하기

- 아이디, 비밀번호 입력
- 로그인, 회원가입
- 쇼핑몰 주문
- 커뮤니티 등
- form 태그 속성
  - method: get, post
  - name: 자바스크립트로 폼을 제어할 때 사용할 폼의 이름을 지정
  - action: form 태그 안의 내용을 처리해줄 서버 프로그램 지정
  - target: action 속성에서 지정한 스크립트 파일을 현재 창이 아닌 다른 위치에 열도록함
- form 요소를 그룹으로 묶는 filedset, legend 태그
- form 요소에 레이블을 붙이는 label 태그

### 1.4.2 사용자 입력을 위한 input 태그

- input 태그의 type 속성
  - text : 한줄 짜리 텍스트, 텍스트 박스
  - password : 비밀번호 필드
  - search : 검색
  - url : URL 주소 입력
  - email : 이메일 주소
  - tel : 전화번호
  - checkbox : 체크박스(중복 체크가능)
  - radio : 라디오 버튼(하나만 체크)
  - number : 숫자
  - range : 숫자를 조절할 수 있는 슬라이드 막대
  - date : 사용자 지역을 기준으로 날짜(연, 월, 일)
  - month : 사용자 지역을 기준으로 연, 월
  - week : 사용자 지역을 기준으로 연, 주
  - time : 사용자 지역을 기준으로 시, 분, 초, 분할 초
  - datetime : 국제표준시(UTC)로 설정된 날짜와 시간(연, 월, 일, 시, 분, 초, 분할초)
  - datetime-local : 사용자 지역을 기준으로 datetime
  - submit : 전송 버튼
  - reset : 리셋 버튼
  - image : submit 버튼 대신 사용할 이미지
  - button : 일반 버튼
  - file : 파일을 첨부할 수 있는 버튼
  - hidden : 사용자에게 보이지 않지만 서버로 넘겨주기 위한 값이 있는 필드
