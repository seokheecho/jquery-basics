##Document Object

[Document 객체]
  Document 객체는 웹 페이지 그 자체를 의미한다.
웹 페이지에 존재하는 HTML 요소에 접근하고자 할 때는 반드시 Document 객체부터 시작해야 한다.

[Document 메소드]
Document 객체는 HTML 요소와 관련된 작업을 도와주는 다양한 메소드를 제공한다.

** HTML 요소의 선택
** HTML 요소의 생성
** HTML 이벤트 핸들러 추가
** HTML 객체의 선택


[HTML 요소의 선택]
HTML 요소를 다루기 위해서는 우선 해당 요소를 선택해야만 한다.

** HTML 태그 이름(tag name)을 이용한 선택
** 아이디(id)를 이용한 선택
** 클래스(class)를 이용한 선택
** name 속성(attribute)을 이용한 선택
** CSS 선택자(selector)를 이용한 선택
** HTML 객체 집합(object collection)을 이용한 선택

***  HTML 요소를 선택하기 위해 제공되는 메소드는 다음과 같다.

 - document.getElementsByTagName(태그이름)
  : 해당 태그 이름의 요소를 모두 선택함.

 - document.getElementById(아이디)
  : 해당 아이디의 요소를 선택함.

 - document.getElementsByClassName(클래스이름)
  : 해당 클래스에 속한 요소를 모두 선택함.

 - document.getElementByName(name속성값)
  : 해당 name 속성값을 가지는 요소를 모두 선택함.

 - document.querySelectorAll(선택자)
  : 해당 선택자로 선택되는 요소를 모두 선택함.

** 이 중에서 document.querySelectorAll() 메소드는 브라우저별로 지원 여부가 다르다. (explore-v9.0, chrome-v1.0, safari-3.2, ...)


[HTML 요소의 생성]
  새로운 HTML 요소를 생성하기 위해 제공되는 메소드는 다음과 같다.
 - document.createElement(HTML요소)
  : 지정된 HTML 요소를 생성함.

 - document.write(텍스트)
  : HTML 출력 스트림을 통해 텍스트를 출력함.


[HTML 이벤트 핸들러 추가]
  HTML 요소에 이벤트 핸들러를 추가하기 위해 제공되는 메소드는 다음과 같다.
 - document.getElementById(아이디).onclick = function(){ 실행할 코드 }
  : 마우스 클릭 이벤트와 연결될 이벤트 핸들러 코드를 추가함.

 - document.getEelementById.onclick = function() {
      하실행할 코드
  }


[HTML 객체의 선택]
  HTML DOM Level 1은 1998년에 정의되어, HTML5에서도 계속 사용되고 있다. 그 후 2004년에는 HTML DOM Level 3가 새롭게 정의되어, Level 1과 같이 사용되고 있다.

  이러한 HTML DOM에서 제공하는 객체 집합(object collection)을 이용하면 HTML 객체를 손쉽게 선택할 수 있다.

 ** 객체 집합 : 설명 - DOM Level
 - document.anchors : name 속성을 가지는 <a>요소를 모두 반환함. - 1
 - document.applets : applet 요소를 모두 반환함. (HTML5에서 제외됨) - 1
 - document.body : <body>요소를 반환함. - 1
 - document.cookie : HTML 문서의 쿠키(cookie)를 반환함. - 1
 - document.domain : HTML 문서가 위치한 서버의 도메인 네임(domain name)을 반환함. - 1
 - document.forms : <form>요소를 모두 반환함. - 1
 - document.images : <img>요소를 모두 반환함. - 1
 - document.links : href 속성을 가지는 <area>요소와 <a>요소를 모두 반환함 - 1
 - document.referrer : 링크(linking)되어 있는 문서의 URI를 반환함. - 1
 - document.title : <title>요소를 반환함. - 1
 - document.URL : HTML 문서의 완전한 URL 주소를 반환함. - 1
 - document.baseURI : HTML 문서의 절대 URI(absolute base URI)를 반환함. - 3
 - document.doctype : HTML문서의 문서 타입(doctype)을 반환함. - 3
 - document.documentElement : <html>요소를 반환함. - 3
 - document.documentMode : 웹 브라우저가 사용하고 있는 모드를 반환함. - 3
 - document.documentURI : HTML 문서의 URI를 반환함. - 3
 - document.domConfig : HTML DOM 설정을 반환함. (더는 사용하지 않음) - 3
 - document.embeds : <embed>요소를 모두 반환함. - 3
 - document.head : <head>요소를 반환함. - 3
 - document.implementation : HTML DOM 구현(implementation)을 반환함. - 3
 - document.inputEncoding : HTML 문서의 문자 인코딩(character set) 형식을 반환함. - 3
 - document.lastModified : HTML 문서의 마지막 갱신 날짜 및 시간을 반환함. - 3
 - document.readyState : HTML 문서의 로딩 상태(loading status)를 반환함. - 3
 - document.scripts : <script>요소를 모두 반환함. - 3
 - document.strictErrorChecking : 오류의 강제 검사 여부를 반환함. - 3


##### 참고 : http://tcpschool.com
