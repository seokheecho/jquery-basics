# Ajax와의 연동_Ajax의 개요

## [Ajax란?]
  Ajax란 Asynchronous JavaScript and XML을 의미한다.
Ajax는 웹 페이지 전체를 다시 로딩하지 않고도, 웹 페이지의 일부분만을 갱신할 수 있게 해준다.
Ajax는 백그라운드 영역에서 서버와 데이터를 교환하여 웹 페이지에 표시해 준다.

## 예제
~~~javascript
$(function() {
    $("#requestBtn").on("click", function() {
        $("#text").load("/examples/media/jquery_ajax_data.txt");
    });
});
~~~


## [Ajax 프레임워크]
  Ajax를 사용하여 손쉽게 개발할 수 있도록 미리 여러 가지 기능들을 포함해 놓은 개발 환경을 Ajax 프레임워크라고 한다.

이러한 Ajax 프레임워크 중에서도 가장 많이 사용되는 대표적인 프레임워크는 다음과 같다.

 - Prototype
 - script.aculo.us
 - dojo
 - jQuery

이외에도 수많은 Ajax 프레임워크가 있지만, 현재 가장 널리 사용되고 있는 Ajax 프레임워크는 바로 제이쿼리(jQuery)이다.


## [제이쿼리와 Ajax]
제이쿼리에서는 Ajax 기능을 손쉽게 사용할 수 있도록 여러 메소드를 제공하고 있다.

이러한 메소드를 사용하면 HTTP 요청(request)을 손쉽게 보낼 수 있다.

또한, 데이터의 종류에 따라 그에 알맞는 메소드를 사용하여 서버에 데이터를 요청할 수 있다.
