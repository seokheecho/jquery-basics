# Navigator Object

## [Navigator 객체]
  navigator 객체는 브라우저 공급자 및 버전 정보 등을 포함한 브라우저에 대한 다양한 정보를 저장하는 객체이다. 이 객체의 이름은 넷스케이프(Netscape)의 초기 웹 브라우저였던 네비게이터(Navigator)에서 유래되었다.


## [브라우저 스니핑(browser sniffing)]
  과거에는 방문자의 웹 브라우저의 종류를 미리 파악하여 조치함으로써, 브라우저 간의 호환성을 유지하였다. 이렇게 호환성을 유지하는 방법을 브라우저 스니핑(browser sniffing)이라고 한다.
navigator 객체는 이러한 브라우저 스니핑에서 사용할 수 있는 다양한 표준 프로퍼티 및 비표준 프로퍼티를 제공한다. 하지만 현재는 이 방법보다 필요한 프로퍼티만을 간단하게 테스트하는 기능 테스팅 방법을 더 많이 사용한다.


## [현재 브라우저의 이름]
  navigator 객체의 appName과 appCodeName 프로퍼티는 현재 사용하고 있는 브라우저의 전체 이름을 반환한다. 하지만 브라우저 간의 호환성을 위해 스니핑 코드로 대부분의 브라우저가 브라우저 이름을 "Netscape"로 사용한다. 또한, 대부분의 브라우저가 브러우저 코드명을 "Mozilla"로 사용한다.


### 예제
~~~javascript
document.write("현재 사용 중인 브라우저의 이름은 " + navigator.appName + "입니다.<br>");

document.write("또한, 해당 브라우저의 코드명은 " + navigator.appCodeName + "입니다.");
~~~

익스플로러 11 버전, 크롬, 파이어폭스와 사파리는 모두 브라우저의 이름을 "Netscape"로 사용한다.
익스플로러 10 이하 버전, 크롬, 파이어폭스, 사파리와 오페라 모두 브라우저 코드명을 "Mozilla"로 사용한다.


** 이 프로퍼티는 웹 표준에서 제외되었으므로, 될 수 있으면 사용하지 않는 것이 좋다.


## [현재 브라우저의 버전]
  navigator 객체의 appVersion과 userAgent 프로퍼티는 현재 사용하고 있는 브라우저의 버전 정보를 문자열로 반환한다. 이 프로퍼티의 결과로 반환되는 문자열에 대한 표준 형식은 따로 명시되어 있지 않다. 따라서 브라우저마다 약간씩 다른 형식의 문자열로 결과를 반환한다. 또한, userAgent 프로퍼티의 결과값은 appVersion 프로퍼티의 정보뿐만 아니라 상세 정보를 추가로 포함한다.

### 예제
~~~javascript
document.write("현재 사용 중인 브라우저의 버전 정보는 " + navigator.appVersion + "입니다.<br><br>");

document.write("userAgent 프로퍼티로 알 수 있는 추가 정보는 " + navigator.userAgent + "입니다.");
~~~

** 이 프로퍼티는 웹 표준에서 제외되었으므로, 될 수 있으면 사용하지 않는 것이 좋다.


## [현재 브라우저가 실행되고 있는 운영체제]
  navigator 객체의 platform 프로퍼티는 현재 브라우저가 실행되고 있는 운영체제를 식별하는 문자열을 반환한다.

### 예제
~~~javascript
document.write("현재 브라우저가 실행되고 있는 운영체제는 " + navigator.platform + "입니다.");
~~~


## [현재 브라우저의 기본 언어 설정]
  navigator 객체의 language 프로퍼티는 현재 사용 중인 브라우저의 기본 언어 설정을 반환한다.

### 예제
~~~javascript
document.write("현재 브라우저의 기본 언어 설정은 " + navigator.language + "입니다.");
~~~


## [자바 애플릿 실행 여부]
  navigator 객체의 `javaEnabled()` 메소드는 현재 사용 중인 브라우저가 자바 애플릿을 실행할 수 있는지를 검사하는 비표준 메소드이다.

### 예제
~~~javascript
document.write("현재 브라우저는 자바 애플릿를 ");
    if (navigator.javaEnabled()) {
        document.write("실행할 수 있습니다.");
    } else {
        document.write("실행할 수 없습니다.");
    }
~~~


## [쿠키(cookie) 사용 여부]
  navigator 객체의 cookieEnabled 프로퍼티는 현재 사용 중인 브라우저가 쿠키를 사용할 수 있는지를 검사하는 비표준 프로퍼티이다.

### 예제
~~~javascript
document.write("현재 브라우저는 쿠키를 ");
    if (navigator.cookieEnabled) {
        document.write("사용할 수 있습니다.");
    } else {
        document.write("사용할 수 없습니다.");
    }
~~~
