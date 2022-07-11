# 7강. 연산자 및 기타 

## 증감 연산자 ( 엄청 중요하진 않지만 편하니까!) 
- C언어의 잔재인데 조금 쓸데없이 복잡합니다. 
- 우리는 a++; 스타일만 사용합시다. <br/>
var a; <br/>
a++;  ( a = a + 1; 과 비슷한 ) <br/>
a = 0; <br/>
a++; <br/>
a--; <br/>


## 비교 연산자 
- 비교 연산자를 수행한 결과값은 Boolean입니다. 
- 비교 연산자에는 >, <, >=, <=, ===(같다), !=(다르다) 등이 있습니다. <br/>
var a = 3; <br/>
var b = 5; <br/>
var c = "5"; <br/>
a > b;       false <br/>
a < b;       true <br/>
b === c;   false <br/>


## 문자열의 길이 구하기 (.length)
var a = "hello" <br/>
a.length; <br/>
  => . 연산자는 객체의 속성을 가져올 때 사용하는 연산자. <br/> 나중에 다시 설명할 예정입니다. <br/>


## 문자열 간단히 조작하기
var a = "KheLLo" <br/>
- a[0];		첫번째 글자 // a[1] 두번째 글자 <br/>
- a[1] = "H"; 	//안 됨.  적용이 되지 않는다. <br/>
- a.slice(1,4);	.slice 자른다 1,2,3 까지 잘라내서 도출된다.

- a.toUpperCase();	  다 대문자로 바뀐다.  	
- a.toLowerCase();    다 소문자로 바뀐다. 

### 변수를 조작한 후에 다른변수에 담아줘야 한다.
### 그래야 적용된 상태를 불러올 수 있다.


## undefined, null, NaN
- undefined: 값이 정의되지 않았다. 
- null: 값이 비어있다. 
- NaN: 값이 아니다.  
- === 계산불가능


## console.log()
- 개발자 콘솔에 뭔가를 찍어주는 메서드입니다.
- 화면에 뭔가를 찍어줄때 사용하는 편리한 메서드 <br/>
var a = 1; <br/>
var b = "더하기"; <br/>
var c = 2; <br/>
console.log(a + " " + b + " " + c + " = " + a + c); <br/>
	=> 1 더하기 2 = 12 로 뜸…;;;;;; <br/> 
console.log(a + " " + b + " " + c + " = " + (a + c)); <br/>
	=> 1 더하기 2 = 3 으로 뜸!!!  <br/>	
    이렇게 해야 원하는 값을 도출해낼수있음

## alert() 과 prompt() 사용해 보기
var ans = prompt("How are you?"); <br/>
alert(ans); <br/>

