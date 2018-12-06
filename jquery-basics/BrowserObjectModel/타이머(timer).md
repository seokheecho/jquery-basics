# 타이머(timer)

## [타이머(timer)]
  window 객체는 일정 시간이 지난 뒤에 함수를 호출할 수 있도록 다음 메소드를 제공한다.

1. `setTimeout()`
2. `setInterval()`

또한, 이렇게 설정된 함수의 호출을 취소할 수 있도록 다음 메소드를 제공한다.

3. `clearTimeout()`
4. `clearInterval()`


## [setTimeout() 메소드]
  `setTimeout()` 메소드는 명시된 시간이 지난 뒤에 지정된 함수를 호출한다.

### 문법
~~~javascript
window.setTimeout(호출할함수, 지연시간);
~~~

이 메소드가 성공적으로 호출되면, 설정된 timeoutID를 반환한다.
이 메소드는 밀리초(milliseconds) 단위로 지연 시간을 설정할 수 있다.

### 예제
~~~javascript
function startTimeout() {
    setTimeout(printCurrentDate, 2000);
}

function printCurrentDate() {
    document.getElementById("date").innerHTML = new Date();
}
~~~


## [setInterval() 메소드]
  `setInterval()` 메소드는 지정된 시간 간격마다 지정된 함수를 반복적으로 호출한다.

### 문법
~~~javascript
window.setInterval(호출할함수, 지연시간);
~~~

이 메소드가 성공적으로 호출되면, 설정된 timeoutID를 반환합니다.
이 메소드는 밀리초(milliseconds) 단위로 시간 간격을 설정할 수 있습니다.

### 예제
~~~javascript
function startInterval() {
    setInterval(printCurrentDate, 2000);
}

function printCurrentDate() {
    document.getElementById("date").innerHTML += new Date() + "<br>";
}
~~~


## [clearTimeout() 메소드]
  `setTimeout()` 메소드의 반환값을 `clearTimeout()` 메소드의 인수로 전달하면, 계획된 함수의 호출을 취소할 수 있다.

### 문법
~~~javascript
window.clearTimeout(timeoutID);
~~~

  이 메소드는 `setTimeout()` 메소드에 의해 함수가 호출되기 전에 실행되어야 호출을 취소할 수 있다.
함수가 호출된 이후에 이 메소드를 호출하면 아무런 동작도 하지 않는다.

### 예제
~~~javascript
var timeoutId;
function startTimeout() {
    timeoutId = setTimeout(printCurrentDate, 2000);
}

function cancelTimeout() {
    clearTimeout(timeoutId);
}

function printCurrentDate() {
    document.getElementById("date").innerHTML += new Date() + "<br>";
}
~~~


## [clearInterval() 메소드]
  `setInterval()` 메소드의 반환값을 `clearInterval()` 메소드의 인수로 전달하면, 반복되는 함수의 호출을 취소할 수 있다.

### 문법
~~~javascript
window.clearInterval(timeoutID);
~~~

### 예제
~~~JavaScript
var timeoutId;
function startInterval() {
    timeoutId = setInterval(printCurrentDate, 2000);
}

function cancelInterval() {
    clearInterval(timeoutId);
}

function printCurrentDate() {
    document.getElementById("date").innerHTML += new Date() + "<br>";
}
~~~
