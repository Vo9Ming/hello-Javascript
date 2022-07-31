# 함수 1 : 함수의 정의와 호출

## 함수의 기초

### 함수란
- 수학의 함수와 상당히 유사합니다. 매개변수 -> (처리) -> 리턴값의 형태를 가집니다. <br/>
f(x) = 2x + 3 <br/>
f(2) = 7 <br/>
f(3) = 9 <br/><br/>

var foo = function(x) { <br/>
    return 2 * x + 3; <br/>
} <br/><br/>

var y= foo(2); <br/>
y = foo(3); <br/>


### 함수 만들기 1
- 매개 변수도 없고, 리턴값도 없는 가장 단순한 형태의 함수를 만들어 봅시다. 출력과 리턴은 전혀 다르다는 걸 기억하세요.<br/>
var foo = function() { <br/>
    console.log("I am function"); <br/>
} <br/><br/>


### 함수 호출
- 함수를 사용하는 걸 함수 호출(call)이라고 합니다. 함수 이름 + 괄호가 필요합니다. <br/>
foo(); <br/>


### 매개변수가 있는 함수 정의하기
var foo2 = function(name) { <br/>
  console.log("hello " + name); <br/>
} <br/><br/>


### 매개변수가 있는 함수 사용해 보기
foo2("honux"); <br/><br/>


#### 예제
- 매개변수를 두 개 사용하는 다음 함수를 구현하고 실행해 봅시다. 어떤 방식으로 동작하는지는 스스로 생각해 보세요.
var repeat = function(text, num) { <br/>
  //code here <br/>
}; <br/><br/>
 
repeat("Hello", 5); <br/>
