# 1. HTML

## 1.1. HTML 구조 파악하기

```html
<!-- 1. 현재 문서가 HTML5 언어로 작성한 웹 문서라는 의미 -->
<!DOCTYPE html>
<!-- 2. <html> ~ </html> 웹 문서의 시작과 끝을 나타내는 태그 -->
<html lang="ko">
  <!-- <head> ~ </head> 웹 브라우저(크롬, 사파리 등)가 웹 문서를 해석하는데 필요한 정보를 입력하는 부분 -->
  <head>
    <!-- 메타정보 : 데이터 관련 -->
    <!-- UTF-8 : 한글 인코딩을 명시하는 태그 -->
    <!-- 웹 사이트의 키워드나 간단한 설명, 제작자 등의 정보를 지정 -->
    <!-- 검색 엔진에서 사이트를 검색할 때 참고 -->
    <meta charset="UTF-8" />

    <!-- 반응형을 위한 메타 태그 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!-- 웹 문서의 키워드 -->
    <meta name="keywords" content="html의 구조" />

    <!-- 웹 문서의 설명 -->
    <meta name="description" content="html의 구조를 알아봅시다" />
    <meta name="author" content="Minkyung Park" />

    <!-- 타이틀 태그 : 웹 문서의 제목, 웹 브라우저의 제목 표시줄에 표시 -->
    <!-- 웹 사이트의 즐겨찾기를 지정할 때도 웹 문서 제목으로 추가 -->
    <title>HTML 구조 파악하기</title>
  </head>
  <!-- body는 실제로 웹 브라우저 화면에 나타나는 내용 -->
  <body>
    <div>
      <header>
        <h1>헤더입니다</h1>
      </header>

      <main>
        <h2>프론트엔드 웹 개발</h2>
        <hr />
        <p>HTML</p>
        <p>CSS</p>
        <p>Javascript</p>
        <p>React</p>
      </main>
      <footer>
        <h3>Footer 입니다</h3>
      </footer>
    </div>
  </body>
</html>
```
