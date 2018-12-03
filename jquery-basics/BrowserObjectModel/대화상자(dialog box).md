# 대화 상자(dialog box)

## [대화 상자(dialog box)]
  사용자에게 보여줄 수 있는 간단한 대화 상자를 만들기 위해 window 객체는 다음과 같은 메소드를 제공한다.

1. `alert()`
2. `confirm()`
3. `prompt()`

## [alert() 메소드]
  window 객체의 `alert()` 메소드는 사용자에게 간단한 메시지를 보여주고, 그에 대한 사용자의 확인을 기다린다.

### 문법
~~~javascript
window.alert("간단한 메시지");
~~~

사용자는 대화 상자의 확인 버튼을 눌러야만 다른 작업을 진행할 수 있다.

### 예제
~~~javascript
function alertDialogBox() {
    alert("확인을 누를 때까지 다른 작업을 할 수 없어요!");
}
~~~

** window 객체의 모든 메소드나 프로퍼티를 사용할 때는 window 라는 접두사를 생략할 수 있다.


## [confirm() 메소드]
  window 객체의 `confirm()` 메소드는 사용자에게 간단한 메시지를 보여주고, 사용자가 확인이나 취소를 누르면 그 결과를 불리언 값으로 반환한다.

### 문법
~~~javascript
window.confirm("간단한 메시지");
~~~

사용자가 확인을 누르면 true를 반환하고, 취소를 누르면 false를 반환한다.

### 예제
~~~javascript
function confirmDialogBox() {
    var str;
        if (confirm("확인이나 취소를 눌러주세요!") == true) {
            str = "당신은 확인을 눌렀습니다!";
        } else {
            str = "당신은 취소을 눌렀습니다!";
        }
    document.getElementById("text").innerHTML = str;
}
~~~

## [prompt() 메소드]
  window 객체의 `prompt()` 메소드는 사용자에게 간단한 메시지를 보여주고, 사용자가 입력한 문자열을 반환한다.


### 문법
~~~javascript
  window.prompt("간단한 메시지" + "입력란의 기본 메시지");
~~~

사용자가 대화 상자에 입력한 텍스트를 문자열 타입으로 반환한다.


### 예제
~~~javascript
function promptDialogBox() {
    var inputStr = prompt("당신의 이름을 입력해 주세요 : ", "홍길동");
        if (inputStr != null) {
            document.getElementById("text").innerHTML = "당신의 이름은 " + inputStr + "입니다.";
        }
}
~~~

  위에서 살펴본 대화 상자 이외에도 `showModalDialog()` 메소드를 이용하면, 좀 더 복잡한 대화 상자를 만들 수 있다.
하지만 이러한 대화 상자는 모두 사용자의 응답이 있을 때까지 브라우저의 실행을 강제로 중단킨다.
따라서 사용자 측면에서 보면 불편할 수도 있으므로, 대화 상자는 될 수 있으면 자주 사용하지 않는 것이 좋다.
