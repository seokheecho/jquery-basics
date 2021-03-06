# 요소의 선택_jQuery 선택자

## [제이쿼리 선택자]
  제이쿼리에서는 CSS 선택자뿐만 아니라 몇몇 비표준 선택자까지도 사용할 수 있다.
이러한 비표준 선택자를 사용하면 선택한 요소를 저장하거나, 그 결과에 대해 필터링까지 할 수 있다.

## [선택한 요소의 저장]
  제이쿼리에서는 선택한 요소들을 변수에 저장하여 사용할 수 있다.
다음 예제는 문서 내의 모든 `<li>` 요소를 선택하여 변수에 저장한 후, 해당 변수를 사용하는 예제이다.

### 예제
~~~javascript
$(function() {
    var items = $("li"); // <li>요소를 모두 선택하여 변수 items에 저장함.
    $("button").on("click", function() {
        $("#len").text("저장된 <li>요소의 총 개수는 " + items.length + "개 입니다.");
    });
});
~~~

하지만 이렇게 저장된 요소들은 변수에 저장될 당시의 요소들만 저장된다.

즉, 요소가 저장된 이후에 문서에 추가되거나 삭제된 요소들을 자동으로 갱신하지는 않는다.


## [선택한 요소의 필터링]
  제이쿼리에서는 선택한 요소 중에서 더욱 세분화된 선택을 하기 위한 필터링을 진행할 수 있다.

다음 예제는 문서 내의 모든 `<li>`요소 중에서 `<span>`요소를 가지고 있는 요소만을 선택하는 예제이다.

### 예제
~~~javascript
$(function() {
    $("button").on("click", function() {
        $("li:has(span)").text("<span>요소를 가지고 있는 아이템이에요!");
    });
});
~~~

필터링에 사용할 수 있는 선택자는 다음과 같다.

|선택자|설명|
|:-----|:-----|
|:eq(n)	| 선택한 요소 중에서 인덱스가 n인 요소를 선택함.|
|:gt(n)	| 선택한 요소 중에서 인덱스가 n보다 큰 요소를 모두 선택함.|
|:lt(n)	| 선택한 요소 중에서 인덱스가 n보다 작은 요소를 모두 선택함.|
|:even	| 선택한 요소 중에서 인덱스가 짝수인 요소를 모두 선택함.|
|:odd	| 선택한 요소 중에서 인덱스가 홀수인 요소를 모두 선택함.|
|:first	| 선택한 요소 중에서 첫 번째 요소를 선택함.|
|:last	| 선택한 요소 중에서 마지막 요소를 선택함.|
|:animated	| 선택한 요소 중에서 애니메이션 효과가 실행 중인 요소를 모두 선택함.|
|:header	| 선택한 요소 중에서 h1부터 h6까지의 요소를 모두 선택함.|
|:lang(언어)	| 선택한 요소 중에서 지정한 언어의 요소를 모두 선택함.|
|:not(선택자)	| 선택한 요소 중에서 지정한 선택자와 일치하지 않는 요소를 모두 선택함.|
|:root	| 선택한 요소 중에서 최상위 루트 요소를 선택함.|
|:target	| 선택한 요소 중에서 웹 페이지 URI의 fragment 식별자와 일치하는 요소를 모두 선택함.|
|:contains(텍스트)	| 선택한 요소 중에서 지정한 텍스트를 포함하는 요소를 모두 선택함.|
|:has(선택자)	| 선택한 요소 중에서 지정한 선택자와 일치하는 자손 요소를 갖는 요소를 모두 선택함.|
|:empty	| 선택한 요소 중에서 자식 요소를 가지고 있지 않은 요소를 모두 선택함.|
|:parent	| 선택한 요소 중에서 자식 요소를 가지고 있는 요소를 모두 선택함.|


## [input 요소의 선택]
  제이쿼리에서는 입력 양식에 관련된 특정 요소를 손쉽게 선택할 수 있다.

### 예제
~~~javascript
$(function() {
    $("button").on("click", function() {
        // 체크되어 있는 요소를 모두 선택함.
        $(":checked").next().text("체크되어 있는 요소는 이 요소입니다.");
    });
});
~~~

특정 `<input>`요소를 선택할 수 있는 선택자는 다음과 같다.

|선택자|설명|
|:-----|:-----|
|:button	| type 속성값이 "button"인 요소를 모두 선택함.|
|:checkbox	| type 속성값이 "checkbox"인 요소를 모두 선택함.|
|:file	| type 속성값이 "file"인 요소를 모두 선택함.|
|:image	| type 속성값이 "image"인 요소를 모두 선택함.|
|:password	| type 속성값이 "password"인 요소를 모두 선택함.|
|:radio	| type 속성값이 "radio"인 요소를 모두 선택함.|
|:reset	| type 속성값이 "reset"인 요소를 모두 선택함.|
|:submit	| type 속성값이 "submit"인 요소를 모두 선택함.|
|:text	| type 속성값이 "text"인 요소를 모두 선택함.|
|:input	| `<input>`, `<textarea>`, `<select>`, `<button>`요소를 모두 선택함.|
|:checked	| type 속성값이 "checkbox" 또는 "radio"인 요소 중에서 체크되어 있는 요소를 모두 선택함.|
|:selected	| `<option>`요소 중에서 선택된 요소를 모두 선택함.|
|:focus	| 현재 포커스가 가지고 있는 요소를 선택함.|
|:disabled	| 비활성화되어있는 요소를 모두 선택함.|
|:enabled	| 활성화되어있는 요소를 모두 선택함.|
