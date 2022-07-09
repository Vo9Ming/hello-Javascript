# 자바스크립트로 무엇을 할 수 있나? 

## 자바스크립트로 할 수 있는 것들

- 자바스크립트는 HTML을 제어할 수 있다.


### 첫 번째 프로그램
- ex1.html 을 작성하고 크롬 브라우저로 연다.
<!-- 
<!DOCTYPE html>
<html>
<body>
<h2>자바스크립트 연습장</h2>
<p id="demo">지금은 몇시인가요?</p>
</body>
</html>
--> 

- 개발자 도구 - 콘솔에서 아래 명령을 실행
var demo = document.getElementById('demo');
demo.innerHTML = Date();

### 두 번째 프로그램
demo.style.color = "red";
demo.style.background = "black";

### 세 번째 프로그램
var demo = document.getElementById('demo');
var size = 10;
function big() {
    demo.style.fontSize = size + "px";
    size = size + 1;            
}
var tid = setInterval(big, 100);