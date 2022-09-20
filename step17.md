# DOM과 HTML

## DOM

- 관련 링크 => https://developer.mozilla.org/ko/docs/Web/API/Document_Object_Model/Introduction

## HTML

- HyperText Markup Language
- WWW의 3요소 중 하나
- 팀 버너스리에 의해 만들어 졌다.

## 엘리먼트 (Element)

- 여는 태그와 닫는 태그로 이루어짐
- 태그 사이에 콘텐츠를 가짐
- 태그 안에 속성과 속성의 값을 가짐
- 닫는 태그가 없는 태그도 있다. (img, br, input)

## 속성(Attributes)

- 객체의 속성과 비슷하게 엘리먼트도 속성을 가질 수 있습니다. <br/>
  < a href="http://codesquad.kr" title="코드스쿼드"> <br/><br/>

### 블록 엘리먼트

- p, h1, div 처럼 줄이 바뀌는 엘리먼트

### 인라인 엘리먼트

- span, img, input, button, a 처럼 줄바뀜이 없는 엘리먼트

## HTML과 JS 분리하기

//// dom.html <br/><br/>

< !DOCTYPE html> <br/>
< meta charset="UTF-8"> <br/>
< html> <br/>
< title>HTML Tutorial< /ttle> <br/>
< head> <br/>
< /head> <br/>
< body> <br/>
< h1 >This is a heading< /h1 > <br/>
< h1 >Another h1 heading< /h1 > <br/>
< p id = 'main' >This is a paragraph.< /p > <br/><br/>

< script src="./dom_test.js">< /script> <br/>
< /body > <br/>
< /html > <br/>
================================================================

//// dom_test.js <br/><br/>

var msg = "Hello"; <br/>
alert(msg); <br/><br/>

================================================================

## DOM (Document Object Model)

- 문서를 객체를 이용해서 계층 구조로 표현함
- 표준: W3CDOM
- 구현체: Gecko, Webkit 등

## html 객체

HTML 문서도 객체로 간주된다. <br/>

- window: 최상위 객체
- document: dom의 최상위 객체이면서 window의 하위 객체 <br/><br/>

var list = document.getElementsByTagName('h1'); <br/>
list[0].innerHTML; <br/>
list[0].innerHTML = "Hello"; <br/><br/>

var list = document.getElementById('main'); <br/>
main.innerHTML = "Hello"; <br/><br/>

## JS로 DOM 제어하기

모든 HTML 엘리먼트는 객체이므로 다른 객체와 마찬가지로 JS로 제어가 가능합니다.

### DOM 객체의 값 바꾸기

var element = document.getElementById('id'); <br/>
element.innerHTML = '값'; <br/>

< h2 >My First Page< /h2 > <br/>
< p id="test" >< /p > <br/>

< script > <br/>
var p = document.getElementById("test"); <br/>
p.innerHTML = "Hello World!"; <br/>
< /script > <br/>
