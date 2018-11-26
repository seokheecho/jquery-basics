## Screen Object

[Screen 객체]
  screen 객체는 사용자의 디스플레이 화면에 대한 다양한 정보를 저장하는 객체이다.
  
[사용자의 화면 크기]
  screen 객체의 width와 height 프로퍼티는 사용자의 디스플레이 화면의 크기를 픽셀 단위로 반환한다.

### 예제
document.write("현재 사용자의 디스플레이 화면의 너비는 " + screen.width + "픽셀입니다.<br>");
document.write("현재 사용자의 디스플레이 화면의 높이는 " + screen.height + "픽셀입니다.<br>");

document.write("현재 브라우저 창의 너비는 " + window.outerWidth + "픽셀입니다.<br>");
document.write("현재 브라우저 창의 높이는 " + window.outerHeight + "픽셀입니다.<br>");

**screen.width와 screen.height는 현재 사용자의 모니터 화면의 크기를 반환한다.
하지만 window.outerWidth와 window.outerHeight는 현재 브라우저 창의 크기를 반환한다.
  
  
[실제 사용할 수 있는 화면 크기]
screen 객체의 availWidth와 availHeight 프로퍼티는 실제 사용할 수 있는 화면의 크기를 픽셀 단위로 반환한다.
이 프로퍼티는 운영체제의 작업 표시줄과 같은 공간을 모두 제외한 크기를 반환한다.

### 예제
document.write("실제 사용할 수 있는 화면의 너비는 " + screen.availWidth + "픽셀입니다.<br>");

document.write("실제 사용할 수 있는 화면의 높이는 " + screen.availHeight + "픽셀입니다.");


[한 색상당 사용할 수 있는 비트수]
screen 객체의 colorDepth 프로퍼티는 사용자 화면에서 한 색상당 사용할 수 있는 비트 수를 반환한다.
대부분의 컴퓨터는 24비트의 트루 컬러(true colors)나 30/36/48비트의 디프 컬러(deep colors)를 사용한다.

### 예제
var bitColorDepth = screen.colorDepth;

document.write("사용자 화면에서 한 색상당 사용할 수 있는 비트수는 " + bitColorDepth + "개입니다.<br>");
document.write("즉, 한 색상은 총 " + Math.pow(2, bitColorDepth) + "가지로 표현됩니다.");

** 트루 컬러에서 한 색상당 사용할 수 있는 비트 수는 224 = 16,777,216 이다.
  
  
[화면 픽셀당 표시할 수 있는 비트수]
screen 객체의 pixelDepth 프로퍼티는 사용자 화면에서 픽셀당 표시할 수 있는 비트 수를 반환한다.

### 예제
var bitPixelDepth = screen.pixelDepth;

document.write("사용자 화면의 한 픽셀당 표시할 수 있는 비트수는 " + bitPixelDepth + "개입니다.<br>");

**대부분의 컴퓨터에서 colorDepth와 pixelDepth는 같은 값을 가진다.





##### 참고 : http://tcpschool.com
