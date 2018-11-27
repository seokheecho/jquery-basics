# jQuery

## [제이쿼리(jQuery)]
  제이쿼리는 자바스크립트 언어를 간편하게 사용할 수 있도록 단순화시킨 오픈 소스 기반의 자바스크립트 라이브러리이다.
제이쿼리를 이용하면 문서 객체 모델(DOM)과 이벤트에 관한 처리를 손쉽게 구현할 수 있다.
또한, Ajax 응용 프로그램 및 플러그인도 제이쿼리를 활용하여 빠르게 개발할 수 있다.

  제이쿼리는 웹 사이트에 자바스크립트를 더욱 손쉽게 활용할 수 있게 해준다.
또한, 제이쿼리를 사용하면 짧고 단순한 코드로도 웹 페이지에 다양한 효과나 연출을 적용할 수 있다.
이러한 제이쿼리는 오늘날 가장 인기 있는 자바스크립트 라이브러리 중 하나이다.

## [제이쿼리의 장점]
  현재 많이 사용되고 있는 자바스크립트 라이브러리는 다음과 같다.
 - 프로토타입(Prototype), 도조(Dojo), GWT(Google Web Toolkit), MochiKit

이렇게 수많은 자바스크립트 라이브러리 중에서도 제이쿼리가 특히 많이 사용되는 이유는 다음과 같다.

1. 제이쿼리는 주요 웹 브라우저의 구버전을 포함한 대부분의 브라우저에서 지원된다.
2. HTML DOM을 손쉽게 조작할 수 있으며, CSS 스타일도 간단히 적용할 수 있다.
3. 애니메이션 효과나 대화형 처리를 간단하게 적용해 준다.
4. 같은 동작을 하는 프로그램을 더욱 짧은 코드로 구현할 수 있다.
5. 다양한 플러그인과 참고할 수 있는 문서가 많이 존재한다.
6. 오픈 라이선스를 적용하여 누구나 자유롭게 사용할 수 있다.

## [제이쿼리 버전]
  제이쿼리는 jQuery Foundation을 통해 버전 개발 및 유지 보수가 진행되고 있다.

현재 각 제이쿼리 버전별 최신 버전은 다음과 같다.

1. 버전 1 : jQuery 1.12.4
2. 버전 2 : jQuery 2.2.4
3. 버전 3 : jQuery 3.2.1


제이쿼리 버전 1은 익스플로러 6, 7, 8 버전에서의 동작까지 모두 지원하는 버전이다.
제이쿼리 버전 2는 버전 1에서 지원하는 익스플로러 6, 7, 8 버전에 대한 지원을 중단한 버전이다.

2014년 10월에 배포된 제이쿼리 버전 3은 제이쿼리의 차세대 표준이다.
제이쿼리 버전 3은 기존 버전과의 호환성을 유지한 채 더욱 간결하게 작성되고, 더욱 빠르게 동작하도록 변경되었다.
2017년 3월에는 제이쿼리 버전 3의 최신 버전인 3.2.1 버전이 발표되었다.

제이쿼리 최신 버전에 대한 더 자세한 사항은 다음 링크를 참고하면 된다.
jQuery Foundation : http://blog.jquery.com =>

 ** 제이쿼리 버전 2와 버전 3는 모두 익스플로러 9 이상에서만 동작한다.
이 때문에 아직도 많은 웹 사이트에서는 제이쿼리 버전 1을 사용하고 있다.

## [제이쿼리 적용]
  제이쿼리는 자바스크립트 라이브러리이므로, 제이쿼리 파일은 자바스크립트 파일(.js 파일) 형태로 존재한다.
따라서 웹 페이지에서 제이쿼리를 사용하기 위해서는 제이쿼리 파일을 먼저 웹 페이지에 로드(load)해야 한다.

웹 페이지에 제이쿼리 파일을 로드하는 방법은 다음과 같다.

1. 제이쿼리 파일을 다운받아 로드하는 방법
2. CDN(Content Delivery Network)을 이용하여 로드하는 방법

[제이쿼리 파일을 다운받아 로드하는 방법]
최신 버전의 제이쿼리 파일은 다음 공식 사이트에서 다운받을 수 있습니다.

 - jQuery.com : http://jquery.com/download

이렇게 다운받은 제이쿼리 파일을 서버에 저장하고, 다음 <script>태그를 웹 페이지의 <head>태그 내에 삽입하면 된다.

### 문법
~~~
<head>
    <script src="/파일경로/제이쿼리파일명.js"></script>
</head>
~~~

### 예제
~~~
<head>
    <script src="/media/jquery-1.12.4.min.js"></script>
</head>
~~~

## [CDN을 이용하여 로드하는 방법]
  CDN(Content Delivery Network)이란 웹 사이트의 접속자가 서버에서 콘텐츠를 다운받아야 할 때, 자동으로 가장 가까운 서버에서 다운받도록 하는 기술이다.
이 기술을 이용하면 특정 서버에 트래픽이 집중되지 않고, 콘텐츠 전송 시간이 매우 빨라지는 장점이 있다.
이러한 CDN을 이용하면 제이쿼리 파일을 서버에 따로 저장하지 않아도 제이쿼리를 사용할 수 있다.

현재 이용할 수 있는 제이쿼리 버전 1의 CDN은 다음과 같으며, 어떤 CDN을 이용하더라도 같은 동작을 한다.

- **CDN(Content Delivery Network)**
1. jQuery.com CDN : <script src="https://code.jquery.com/jquery-1.12.4.min.js"></script>
2. 구글 CDN       : <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
3. MS CDN         : <script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-1.12.4.min.js"></script>
4. CDNJS CDN      : <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
5. jsDelivr CDN   : <script src="https://cdn.jsdelivr.net/jquery/1.12.4/jquery.min.js"></script>

### 예제
~~~
<head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
</head>
~~~
