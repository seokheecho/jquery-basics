##Location Object

[Location 객체]
  location 객체는 현재 브라우저에 표시된 HTML 문서의 주소를 얻거나, 브라우저에 새 문서를 불러올 때 사용할 수 있다.
이 객체는 Window 객체의 location 프로퍼티와 Document 객체의 location 프로퍼티에 같이 연결되어 있다.

location 객체의 프로퍼티와 메소드를 이용하면, 현재 문서의 URL 주소를 다양하게 해석하여 처리할 수 있다.


[현재 문서의 URL 주소]
  location 객체의 href 프로퍼티는 현재 문서의 전체 URL 주소를 문자열로 반환한다.
- document.write("현재 문서의 주소는 " + location.href + "입니다.");


[현재 문서의 호스트 이름]
  location 객체의 hostname 프로퍼티는 현재 문서의 인터넷 호스트 이름을 반환합니다.
- document.write("현재 문서의 호스트 이름은 " + location.hostname + "입니다.");

** host, hostname, port, hash와 같은 location 객체의 주요 프로퍼티는 URL 주소의 다양한 특성을 저장하고 있다.
이와 같은 프로퍼티는 Link 객체를 통해서도 제공된다.


[현재 문서의 파일 경로명]
  location 객체의 pathname 프로퍼티는 현재 문서의 파일 경로명을 반환한다.
- document.write("현재 문서의 파일 경로명은" + location.pathname + "입니다.");

** 호스트 이름(host name)과 파일 경로명(path name)을 합쳐 URL(Uniform Resource Locator)이라고 부른다.
이러한 URL은 브라우저가 웹 서버로 컨텐츠를 요청할 때, 해당 컨텐츠가 어디에 있는지를 알려주기 위한 규약이다.


[현재 창에 문서 불러오기]
  location 객체의 assign() 메소드는 브라우저 창에 지정된 URL 주소에 존재하는 문서를 불러온다.

반면에 replace() 메소드는 새 문서를 불러오기 전에, 현재 문서를 브라우저의 히스토리에서 제거한다는 점이 assign() 메소드와 다르다.

location 객체의 reload() 메소드는 브라우저 창에 현재 문서를 다시 불러온다.

### 예제
function openDocument() {
    location.assign("/index.php");
}

function openDocumentWithReplace() {
    location.replace("/index.php");
}

** 현재 문서를 브라우저의 히스토리에서 제거한다는 의미는 브라우저의 뒤로 가기 버튼을 눌러도 이전 페이지로 다시 돌아갈 수 없다는 의미이다.

** 기본적으로 문서(.php, .html, ...)를 호출하며, 파일경로(path name)+문서?key=value 도 가능하다. ex) /examples/tryit/tryhtml.php?filename=js_bom_location_04




##### 참고 : http://tcpschool.com
