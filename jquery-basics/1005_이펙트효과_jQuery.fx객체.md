# 이펙트 효과_jQuery.fx 객체

## [jQuery.fx 객체]
  제이쿼리의 jQuery.fx 객체는 이펙트 효과가 구현되는 방법을 제어하는 다양한 프로퍼티를 가지고 있다.

1. `jQeury.fx.speeds`
2. `jQeury.fx.interval`
3. `jQeury.fx.off`


## [jQuery.fx.speeds 프로퍼티]
  jQuery.fx 객체의 speeds 프로퍼티는 "slow", "normal", "fast" 값을 가지고 이펙트 효과의 속도를 나타낸다.

제이쿼리에서 제공하는 jQuery.fx.speed 프로퍼티의 기본값은 다음과 같다.

|프로퍼티 값|밀리초(milisecond)|
|:-----:|:-----:|
|fast	| 200|
|normal	| 400|
|slow	| 600|

  이러한 속도의 기본값을 speeds 프로퍼티를 이용하여 변경할 수도 있다.

### 예제
~~~javascript
  $(function() {
      $("#toggleBtn").on("click", function() {
          // id가 "divBox"인 요소를 빠르게(0.2초에 걸쳐) 올라가면서 사라지거나 내려오면서 나타나게 함.
          $("#divBox").slideToggle("fast");
      });
      $("#setBtn").on("click", function() {
          // jQuery.fx 객체의 speeds 프로퍼티의 fast의 기본값을 1초로 변경함.
          jQuery.fx.speeds.fast = 1000;
      });
  });
~~~


## [jQuery.fx.interval 프로퍼티]
  jQuery.fx 객체의 interval 프로퍼티는 이펙트 효과가 보여지는 동안의 초당 프레임 수를 나타낸다.

연속적인 프레임에서의 초당 프레임 수는 13으로 기본 설정되어 있다.

이러한 초당 프레임 수를 interval 프로퍼티를 이용하여 사용 목적에 맞게 변경할 수 있다.


## [jQuery.fx.off 프로퍼티]
  jQuery.fx 객체의 off 프로퍼티를 true로 설정하면, 모든 이펙트 효과를 사용할 수 없게 된다.

이렇게 이펙트 효과가 비활성화되면, 이펙트 효과는 실행되지 않으며 이펙트 효과의 마지막 상태로 즉시 변경된다.

off 프로퍼티는 특히 구형 버전의 브라우저를 다룰 때 유용하게 사용될 수 있다.

### 예제
~~~javascript
$(function() {
    $("#toggleBtn").on("click", function() {
        // id가 "divBox"인 요소를 1초에 걸쳐 올라가면서 사라지거나 내려오면서 나타나게 함.
        $("#divBox").slideToggle(1000);
    });
    $("#forbidBtn").on("click", function() {
        // jQuery.fx 객체의 off 프로퍼티를 true로 설정함.
        jQuery.fx.off = true;
    });
});
~~~


## [jQuery.fx 객체 프로퍼티]
|프로퍼티|설명|
|:-----|:-----|
|jQeury.fx.speeds	| 밀리초에 해당하는 "slow", "fast" 등의 값을 가지고 이펙트 효과의 속도를 나타냄.|
|jQeury.fx.interval	| 이펙트 효과가 보여지는 동안의 초당 프레임 수를 나타냄.|
|jQeury.fx.off	| 모든 이펙트 효과를 사용할 수 없도록 비활성화시킴.|
