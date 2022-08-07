# 함수 2 : 함수와 리턴값

## 함수와 리턴 값
- 리턴 값이 있는 함수 정의하기
- 리턴 값이 있을 경우 함수를 호출해서 변수에 값을 넣을 수 있습니다. <br/><br/>

var five = function() { <br/>
  return 5; <br/>
} <br/><br/>

var n = five(); <br/> 
console.log(n); <br/><br/><br/><br/>


* 리턴이 없는 함수를 변수에 할당하면? <br/>
var foo = function() { <br/>
    console.log(5); <br/>
} <br/>
var n = foo(); <br/>
console.log(n); <br/><br/>

* 아무 값도 없는 리턴 사용하기 <br/>
return 으로 함수를 종료하는데 사용할 수 있다. <br/>
var test1 = function(text) { <br/>
  if (text === "exit") { <br/>
    return; <br/>
  }    <br/>
  console.log("보이나요?");     <br/>
} <br/><br/>

test1("hoho"); <br/>
test1("exit"); <br/>

## 함수를 사용하면
* 가독성이 좋아짐
* 유지보수를 잘 하게 됨

## 함수 어떻게 만들까?
* 매개 변수와 리턴을 적극적으로 활용하자.
* 줄 수가 지나치게 길어지면 함수로 빼자. (10줄 정도)
* 인덴트가 지나치게 깊어져도 함수로 빼자.
* 함수는 반드시 한 가지 일만 하도록 하자. <br/>
(Option) 2중 루프를 한 번에 빠져 나가기 <br/>
- `break` 명령은 한 번에 한 루프만 빠져나갑니다.
- 함수의 `return` 을 이용하면 2중 루프를 한 번에 종료할 수 있습니다. 
