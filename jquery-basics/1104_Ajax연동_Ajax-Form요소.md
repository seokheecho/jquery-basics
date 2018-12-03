# Ajax와의 연동_Ajax와 Form 요소

## [Ajax와 Form 요소]
  Ajax에서는 서버와의 비동기식 통신을 위해 form 요소를 통해 입력받은 데이터를 직렬화(serialization)하여 전송한다.

이때 직렬화(serialization)란 입력받은 여러 데이터를 하나의 쿼리 문자열로 만드는 것을 의미한다.
이렇게 함으로써 form 요소를 통해 입력받은 데이터를 한 번에 서버로 보낼 수 있게 된다.


## [직렬화(serialization)]
  제이쿼리에서는 HTML form 요소를 통해 입력된 데이터의 직렬화 작업을 매우 간단하게 수행할 수 있다.
`.serialize()` 메소드와 `.serializeArray()` 메소드를 이용하여 손쉽게 데이터를 직렬화할 수 있다.

`.serialize()` 메소드는 HTML form 요소를 통해 입력된 데이터를 쿼리 문자열로 변환한다.
`.serializeArray()` 메소드는 `serialize()` 메소드와는 달리 입력된 데이터를 문자열이 아닌 배열 객체로 변환한다.

### 예제
~~~javascript
$(function() {
    $("form").on("submit", function(event) {  // <form>요소에 "submit" 이벤트가 발생할 때,
        event.preventDefault();               // 서버로 전송하지 않음.
        $("#text").html($(this).serialize()); // 입력받은 데이터를 직렬화하여 나타냄.
    });
});
~~~

** 한글이 포함된 입력 데이터가 쿼리 문자열로 변환될 때는 퍼센트 인코딩(percent-encoding)을 통해 변환된다.
이때 모든 한글 문자는 퍼센트 기호(%)를 포함한 16진수 값으로 변환된다.
