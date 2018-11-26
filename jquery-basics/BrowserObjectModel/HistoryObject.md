## History Object

[History 객체]
  history 객체는 브라우저의 히스토리 정보를 문서와 문서 상태 목록으로 저장하는 객체이다.
자바스크립트는 사용자의 개인 정보를 보호하기 위해 이 객체에 접근하는 방법을 일부 제한하고 있다.


[히스토리 목록의 개수]
  history 객체의 length 프로퍼티는 브라우저 히스토리 목록의 개수를 반환한다.

### 예제
function openDocument() {
    location.assign("/javascript/js_bom_history");
}

document.getElementById("text").innerHTML =
"현재 브라우저의 히스토리 목록의 개수는 " + history.length + "개 입니다.";


[히스토리 목록 접근하기]
  history 객체에는 브라우저의 뒤로 가기와 앞으로 가기 버튼과 같은 동작을 하는 back()과 forward() 메소드를 가지고 있다.
또한, go() 메소드를 이용하면 인수로 전달받는 정수만큼 히스토리 목록 사이를 이동할 수도 있다.
다음 예제는 back() 메소드를 이용하여 브라우저의 히스토리 목록에서 바로 이전 URL로 이동하는 예제이다.
이 버튼은 브라우저의 이전 페이지로 가기 버튼과 같은 동작을 한다.


다음 예제는 back() 메소드를 이용하여 브라우저의 히스토리 목록에서 바로 이전 URL로 이동하는 예제이다.
이 버튼은 브라우저의 이전 페이지로 가기 버튼과 같은 동작을 한다.

### 예제
<button onclick="goBack()">이전 페이지로 가기</button>
...
<script>
    
    function goBack() {
        window.history.back();
    }
    
</script>


다음 예제는 go() 메소드를 이용하여 back() 메소드와 같은 동작을 하도록 만든 예제이다.

### 예제
<button onclick="go()">이전 페이지로 가기</button>
...
<script>

    function go() {
        window.history.go(-1);
    }

</script>

위의 예제에서처럼 go() 메소드에 인수로 -1을 전달하면 back() 메소드와 같은 동작을 하게 된다.

 
다음 예제는 forward() 메소드를 이용하여 브라우저의 히스토리 목록에서 바로 다음 URL로 이동하는 예제이다.
이 버튼은 브라우저의 다음 페이지로 가기 버튼과 같은 동작을 한다.

### 예제
<button onclick="goForward()">다음 페이지로 가기</button>
...
<script>
    
    function goForward() {
        window.history.forward();
    }

</script>


##### 참고 : http://tcpschool.com
