# Window Object

## [Window 객체]
  window 객체는 웹 브라우저의 창(window)을 나타내는 객체로, 대부분의 웹 브라우저에서 지원하고 있다.

자바스크립트의 모든 객체, 전역 함수, 전역 변수들은 자동으로 window 객체의 프로퍼티가 된다.

window 객체의 메소드는 전역 함수이며, window 객체의 프로퍼티는 전역 변수가 된다.

문서 객체 모델(DOM)의 요소들도 모두 window 객체의 프로퍼티가 된다.


## [브라우저 창 크기 조절]
  window 객체의 innerHeight와 innerWidth 프로퍼티를 이용하면, 브라우저의 창 크기를 설정할 수 있다.

여기서 브라우저 창이란 웹 브라우저의 뷰포트(viewport)를 의미하며, 브라우저의 툴바나 스크롤 바는 포함되지 않는다.

### 문법
~~~javascript
// 기본 문법
window.innerHeight
window.innerWidth

// 익스플로러 5부터 7버전만을 위한 문법 1
document.documentElement.clientHeight
document.documentElement.clientWidth

// 익스플로러 5부터 7버전만을 위한 문법 2
document.body.clientHeight
document.body.clientWidth
~~~

### 예제
~~~javascript
var windowWidth = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth;

var windowHeight = window.innerHeight || document.documentElement.clientHeight || document.body.clientHeight;

document.write("웹 브라우저의 너비는 " + windowWidth + "픽셀이고, 높이는 " + windowHeight + "픽셀입니다.");
~~~

  window 객체의 모든 메소드나 프로퍼티를 사용할 때는 window라는 접두사를 생략할 수 있다.

따라서 위의 예제에서 window.innerWidth 대신 그냥 innerWidth를 사용해도 정상적으로 동작한다.

다음 예제는 window 접두사를 생략할 수 있는 다양한 예를 보여준다.

### 예제
~~~javascript
alert("전역 함수 호출시 window 접두사 생략 가능함!");                     // 전역 함수
document.write("현재 브라우저의 수평 위치는 " + screenX + "입니다.<br>"); // 전역 변수
document.write("현재 브라우저의 수직 위치는 " + screenY + "입니다.<br>"); // 전역 변수
document.write(document.title);                                           // 전역 객체
~~~

  위의 예제처럼 자바스크립트의 모든 전역 객체, 전역 함수, 전역 변수를 사용할 때는 window 접두사를 생략할 수 있다.

screenX는 해당 브라우저 창의 왼쪽 모서리와 사용자 스크린의 왼쪽 모서리 사이의 거리를 반환한다.
또한, screenY는 해당 브라우저 창의 위쪽 모서리와 사용자 스크린의 위쪽 모서리 사이의 거리를 반환한다.

브라우저 새 창 열기
window 객체의 `open()` 메소드를 이용하면, 새로운 브라우저 창을 열 수 있다.

또한, 새로운 브라우저 창의 세부적인 옵션들도 일일이 설정할 수 있다.


이 옵션에서 사용할 수 있는 프로퍼티는 다음 그림과 같다.

![JavaScript_Browser](http://tcpschool.com/lectures/img_js_browser_window.png)


다음 예제는 메뉴바, 주소창, 크기조절 손잡이, 스크롤 바, 상태 바만을 가지는 새로운 브라우저 창을 여는 예제이다.

### 예제
~~~javascript
var newWindowObj;
// 변수 strWindowFeatures를 통해 새롭게 여는 브라우저 창의 옵션들을 일일이 설정할 수 있음.
var strWindowFeatures = "menubar = yes,location = yes,resizable = yes,scrollbars = yes,status = yes";

function openWindow() {
    newWindowObj = window.open("/html/intro", "HTML 개요", strWindowFeatures);
}
~~~


## [브라우저 창 닫기]
  window 객체의 `close()` 메소드를 이용하면, 현재 브라우저나 특정 브라우저 창을 닫을 수 있다.

### 예제
~~~javascript
function openWindow() {
    newWindowObj = window.open("/html/intro", "HTML 개요", strWindowFeatures);
}

function closeNewWindow() { // 새롭게 연 브라우저 창을 window 객체를 이용하여 다시 닫을 수 있음.
    newWindowObj.close();
}
~~~


## [Document 객체]
  window 객체의 가장 중요한 프로퍼티 중 하나가 바로 document 객체입니다.
document 객체는 브라우저 창에 표시되는 내용에 해당하는 문서(document)를 나타내는 객체입니다.
