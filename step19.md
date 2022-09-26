# 스코프

## Scope란?

- 변수의 유효범위
- 검색키워드: javascript scope

## 전역 변수

함수 외부에서 선언된 변수 많이 쓰면 좋지 않습니다. 가급적이면 사용하지 않는 게 좋습니다.

## 지역 변수

함수 안에서 선언된 변수 외부에서 사용할 수 없다.

## 자동 전역 변수

함수 안에서 var 없이 선언하면 자동 전역 변수가 된다. 절대로 이렇게 하면 안 됩니다!

## 매개변수의 스코프

함수의 매개 변수는 자동으로 지역 변수 취급

## for문 안에서 사용된 변수의 스코프

언어마다 다른데 자바스크립트어세는 그냥 for문 바깥에서 선언된 것과 동일한 효과입니다.

## const와 let

ES6의 새로 등장한 문법으로 var 와는 조금 다르게 동작합니다. <br/>
일반적으로 연습할 때는 const와 let을 쓰는 걸 권장합니다. <br/>
let은 블록 범위 스코프를 가지고 있습니다. <br/>
일단 변수 선언은 무조건 const로 하자. const로 안 되는 상황 발생시에 let을 쓰자. <br/><br/>

- const
  const 선언은 블록 범위의 상수를 선언합니다. 상수의 값은 재할당할 수 없으며 다시 선언할 수도 없습니다. <br/><br/>

1.  구문 <br/>
    const name1 = value1 [, name2 = value2 [, ... [, nameN = valueN]]]; <br/>

    매개변수 <br/><br/>

    - nameN : 상수의 이름. 아무 유효한 식별자를 사용할 수 있습니다. <br/>

    - valueN : 상수의 값. 아무 유효한 표현식이나 가능합니다. <br/>

2.  설명 <br/>
    이 선언은 선언된 함수에 전역 또는 지역일 수 있는 상수를 만듭니다. <br/>
    상수 초기자(initializer)가 필요합니다. <br/>
    즉 선언되는 같은 문에 그 값을 지정해야 합니다(이는 나중에 변경될 수 없는 점을 감안하면 말이 됩니다). <br/><br/>

    상수는 let 문을 사용하여 정의된 변수와 마찬가지로 블록 범위(block-scope)입니다. <br/>
    상수의 값은 재할당을 통해 바뀔 수 없고 재선언될 수 없습니다. <br/><br/>

    let에 적용한 "일시적 사각 지대"에 관한 모든 고려는, const에도 적용합니다. <br/><br/>

    상수는 같은 범위의 상수 또는 변수와 그 이름을 공유할 수 없습니다. <br/><br/>

- let <br/>
  let 명령문은 블록 스코프의 범위를 가지는 지역 변수를 선언하며, 선언과 동시에 임의의 값으로 초기화할 수도 있습니다. <br/><br/>

1.  구문 <br/>
    let var1 [= value1] [, var2 [= value2]] [, ..., varN [= valueN]]; <br/><br/>

    매개변수 <br/>

    - nameN : 변수 이름. 모두 유효한 JavaScript 식별자여야 합니다. <br/>

    - valueN (Optional) : 각각의 변수 선언에 대해, 유효한 JavaScript 표현식을 지정해 변수의 초기 값을 지정할 수 있습니다. <br/><br/>

    이 구문 대신 구조 분해 할당을 사용해서 변수를 선언할 수도 있습니다. <br/>
    let { bar } = foo; // foo = { bar: 10, baz: 12 }; <br/>
    /_ 10의 값을 가진 'bar' 변수를 생성 _/ <br/><br/>

2.  설명 <br/>
    let을 사용하면 블록 명령문이나 let을 사용한 표현식 내로 범위가 제한되는 변수를 선언할 수 있습니다. <br/>
    이는 let이 var 키워드와 다른 점으로, var는 변수를 블록을 고려하지 않고 현재 함수 (또는 전역 스코프) <br/>
    어디에서나 접근할 수 있는 변수를 선언합니다. <br/>
    또한 let은 파서가 구문을 평가해야만 변수를 값으로 초기화(아래 참고)한다는 점도 var와 다릅니다. <br/><br/>

    const와 마찬가지로 let 역시 전역 범위 선언에 사용(최상위 스코프 선언)해도 window 객체에 새로운 속성을 추가하지 않습니다. <br/>
    참고: let 변수가 가진 다양한 문제는, let 변수 선언을 현재 스코프의 맨 위에서 수행해서 피할 수 있습니다. <br/>
    (가독성에 영향을 줄 수 있습니다) <br/><br/>

3.  예제 <br/>
    - 스코프 규칙 <br/>
      let으로 선언한 변수는 자신을 선언한 블록과 모든 하위 블록을 스스로의 스코프로 가집니다. <br/>
      이런 점에서는 let이 var와 유사합니다. 그러나 둘의 중요한 차이는, var의 경우 스코프가 '자신을 선언한 블록'이 아니라, <br/>
      자신의 선언을 포함하는 함수라는 점입니다. <br/><br/>

function varTest() { <br/>
var x = 1; <br/>
if (true) { <br/>
var x = 2; // 같은 변수! <br/>
console.log(x); // 2 <br/>
} <br/>
console.log(x); // 2 <br/>
} <br/><br/>

function letTest() { <br/>
let x = 1; <br/>
if (true) { <br/>
let x = 2; // 다른 변수 <br/>
console.log(x); // 2 <br/>
} <br/>
console.log(x); // 1 <br/>
} <br/><br/>

프로그램 최상위에서 사용할 경우 var는 전역 객체에 속성을 추가하지만 let은 추가하지 않습니다. <br/><br/>

var x = 'global'; <br/>
let y = 'global'; <br/>
console.log(this.x); // "global" <br/>
console.log(this.y); // undefined <br/><br/>

4.  비공개 멤버 모사 <br/>
    - 생성자 (en-US)와 let을 함께 사용하면 클로저를 사용하지 않아도 비공개 멤버를 나타낼 수 있습니다. <br/><br/>

var Thing; <br/><br/>

{ <br/>
let privateScope = new WeakMap(); <br/>
let counter = 0; <br/><br/>

Thing = function() { <br/>
this.someProperty = 'foo'; <br/><br/>

    privateScope.set(this, {
      hidden: ++counter,
    });

<br/>
}; <br/><br/>

Thing.prototype.showPublic = function() { <br/>
return this.someProperty; <br/>
}; <br/><br/>

Thing.prototype.showPrivate = function() { <br/>
return privateScope.get(this).hidden; <br/>
}; <br/>
} <br/><br/>

console.log(typeof privateScope); <br/>
// "undefined" <br/><br/>

var thing = new Thing(); <br/><br/>

console.log(thing); <br/>
// Thing {someProperty: "foo"} <br/><br/>

thing.showPublic(); <br/>
// "foo" <br/><br/>

thing.showPrivate(); <br/>
// 1 <br/><br/>

클로저를 사용하면 var를 써도 위와 동일한 은닉 패턴을 구현할 수 있습니다. <br/>
그러나 이 경우, 위 코드와 같은 단순 블록 스코프를 사용할 수 없으며 함수 스코프(보통 모듈 패턴의 IIFE)가 필요합니다. <br/><br/>

5.  재선언 <br/>
    - 같은 변수를 같은 함수나 블록 스코프 안에서 다시 선언하려고 시도하면 SyntaxError가 발생합니다. <br/><br/>

if (x) { <br/>
let foo; <br/>
let foo; // SyntaxError <br/>
} <br/><br/>

switch 명령문에는 블록이 하나밖에 없으므로 이 오류를 자주 마주칠 수 있습니다. <br/><br/>

let x = 1; <br/>
switch(x) { <br/>
case 0: <br/>
let foo; <br/>
break; <br/><br/>

case 1: <br/>
let foo; // 재선언으로 인한 SyntaxError <br/>
break; <br/>
} <br/><br/>

그러나 분기에 블록을 배치하면 블록 스코프도 생성하므로 재선언으로 인한 오류가 발생하지 않습니다. <br/>
let x = 1; <br/><br/>

switch(x) { <br/>
case 0: { <br/>
let foo; <br/>
break; <br/>
} <br/>
case 1: { <br/>
let foo; <br/>
break; <br/>
} <br/>
} <br/><br/>

6.  시간상 사각지대 <br/>

    - let 변수는 초기화하기 전에는 읽거나 쓸 수 없습니다(선언 구문에 초기 값을 지정하지 않은 경우 undefined로 초기화함). <br/>
      초기화 전에 접근을 시도하면 ReferenceError가 발생합니다. <br/>
      참고: var 변수와 다른 점으로, var의 경우 선언 전에 접근할 시 undefined입니다. <br/><br/>

    변수 스코프의 맨 위에서 변수의 초기화 완료 시점까지의 변수는 "시간상 사각지대"(Temporal Dead Zone, TDZ)에 들어간 변수라고 표현합니다. <br/><br/>

function do_something() { <br/>
console.log(bar); // undefined <br/>
console.log(foo); // ReferenceError <br/>
var bar = 1; <br/>
let foo = 2; <br/>
} <br/><br/>

"시간상" 사각지대인 이유는, 사각지대가 코드의 작성 순서(위치)가 아니라 코드의 실행 순서(시간)에 의해 형성되기 때문입니다. <br/>
예컨대 아래 코드의 경우 let 변수 선언 코드가 그 변수에 접근하는 함수보다 아래에 위치하지만, <br/>
함수의 호출 시점이 사각지대 밖이므로 정상 동작합니다. <br/><br/>

{ <br/>
// TDZ가 스코프 맨 위에서부터 시작 <br/>
const func = () => console.log(letVar); // OK <br/><br/>

    // TDZ 안에서 letVar에 접근하면 ReferenceError

    let letVar = 3; // letVar의 TDZ 종료
    func(); // TDZ 밖에서 호출함

}<br/><br/>

7.  TDZ와 typeof <br/>
    - typeof 연산자를 TDZ 내의 let 변수에 사용해도 ReferenceError가 발생합니다. <br/><br/>

console.log(typeof i); // ReferenceError <br/>
let i = 10; <br/><br/>

선언조차 하지 않은 변수, 또는 undefined를 값으로 가진 변수와 다른 점입니다. <br/><br/>

console.log(typeof undeclaredVariable); // undefined 출력 <br/><br/>

8.  어휘적 스코프와 결합한 TDZ <br/>
    아래 코드는 주석으로 표기한 지점에서 ReferenceError가 발생합니다. <br/><br/>

function test(){ <br/>
var foo = 33; <br/>
if(foo) { <br/>
let foo = (foo + 55); // ReferenceError <br/>
} <br/>
} <br/>
test(); <br/><br/>

    바깥 스코프의 var foo가 값을 가지므로 if 블록 또한 평가됩니다.
    그러나 어휘적 스코프로 인해, var foo의 값은 블록 내에서 사용할 수 없습니다.
    이곳의 foo 식별자는 let foo를 가리키기 때문입니다. 따라서 (foo + 55) 표현식은 let foo의 초기화가 끝나지 않은,
    즉 TDZ의 내부이며 ReferenceError가 발생하게 되는 것입니다.

    아래와 같은 코드에서는 이 현상으로 인해 상당한 혼란을 겪을 수 있습니다.
    반복문의 let n of n.a는 for 블록의 스코프에 속하므로,
    식별자 n.a는 반복문 스스로가 선언(let n)하는 n 객체의 a 속성을 가리킵니다.
    그리고 n의 선언 후 초기화가 아직 끝나지 않았으므로 n.a는 let n의 TDZ에 속합니다.

<br/>
function go(n) { <br/>
// 이 n은 매개변수 n <br/>
console.log(n); // Object {a: [1,2,3]} <br/><br/>

for (let n of n.a) { // ReferenceError <br/>
console.log(n); <br/>
} <br/>
} <br/><br/>

go({a: [1, 2, 3]}); <br/><br/>

9.  기타 예제 <br/>
    - 블록 내에서 사용한 경우 let은 변수의 스코프를 해당 블록으로 제한합니다. var는 스코프를 함수로 제한한다는 차이에 주의하세요. <br/>

var a = 1; <br/>
var b = 2; <br/><br/>

if (a === 1) { <br/>
var a = 11; // 전역 변수 <br/>
let b = 22; // if 블록 변수 <br/><br/>

console.log(a); // 11 <br/>
console.log(b); // 22 <br/>
} <br/><br/>

console.log(a); // 11 <br/>
console.log(b); // 2 <br/>

    그러나 var와 let을 아래와 같이 사용하면 SyntaxError입니다.
    호이스팅으로 인해 var가 블록 최상단으로 끌어올려져, 변수 재선언을 하는 것과 같아지기 때문입니다.

<br/>
let x = 1; <br/><br/>

{ <br/>
var x = 2; // 재선언으로 인한 SyntaxError <br/>
} <br/><br/>

## 호이스팅

JavaScript에서 호이스팅(hoisting)이란, <br/>
인터프리터가 변수와 함수의 메모리 공간을 선언 전에 미리 할당하는 것을 의미합니다. <br/>
var로 선언한 변수의 경우 호이스팅 시 undefined로 변수를 초기화합니다. <br/>
반면 let과 const로 선언한 변수의 경우 호이스팅 시 변수를 초기화하지 않습니다. <br/><br/>

호이스팅을 설명할 땐 주로 "변수의 선언과 초기화를 분리한 후, <br/>
선언만 코드의 최상단으로 옮기는" 것으로 말하곤 합니다. <br/>
따라서 변수를 정의하는 코드보다 사용하는 코드가 앞서 등장할 수 있습니다. <br/>
다만 선언과 초기화를 함께 수행하는 경우, 선언 코드까지 실행해야 변수가 초기화된 상태가 됨을 주의하세요. <br/><br/>

\*\* 참고: 호이스팅은 (let과 const를 포함한) ECMAScript® 2015 언어 명세 이전의 표준 명세에는 나타나지 않았습니다. <br/>
당시에는 호이스팅이 JavaScript에서 실행 맥락, 특히 생성 및 실행 단계의 동작 방식을 설명하는 일반적인 방법이었습니다. <br/><br/>

- 기술 예제 <br/>
  JavaScript는 함수의 코드를 실행하기 전에 함수 선언에 대한 메모리부터 할당합니다. <br/>
  덕분에 함수를 호출하는 코드를 함수 선언보다 앞서 배치할 수 있습니다. <br/><br/>

  예를 들어, <br/><br/>

function catName(name) { <br/>
console.log("제 고양이의 이름은 " + name + "입니다"); <br/>
} <br/><br/>

catName("호랑이"); <br/><br/>

/_ <br/>
결과: "제 고양이의 이름은 호랑이입니다" <br/>
_/ <br/><br/>

위의 코드 조각이 일반적으로 코드를 작성하는 순서라면, 함수를 선언하기 전에 먼저 호출했을 때의 예제도 보겠습니다. <br/><br/>

catName("클로이"); <br/><br/>

function catName(name) { <br/>
console.log("제 고양이의 이름은 " + name + "입니다"); <br/>
} <br/><br/>

/_ <br/>
결과: "제 고양이의 이름은 클로이입니다" <br/>
_/ <br/><br/>

함수 호출이 함수 자체보다 앞서 존재하지만, 그럼에도 불구하고 이 코드 역시 동작합니다. 이것이 JavaScript에서 실행 맥락이 동작하는 방식입니다. <br/><br/>

호이스팅은 다른 자료형과 변수에도 잘 작동합니다. 변수를 선언하기 전에 먼저 초기화하고 사용할 수 있는 것입니다. <br/><br/>

- 선언만 호이스팅 대상 <br/>
  JavaScript는 초기화를 제외한 선언만 호이스팅합니다. 변수를 먼저 사용하고 그 후에 선언 및 초기화가 나타나면, <br/>
  사용하는 시점의 변수는 기본 초기화 상태(var 선언 시 undefined, 그 외에는 초기화하지 않음)입니다. <br/>
  예를 들어, <br/>

console.log(num); // 호이스팅한 var 선언으로 인해 undefined 출력 <br/>
var num; // 선언 <br/>
num = 6; // 초기화 <br/><br/>

반면, 다음 예제는 선언 없이 초기화만 존재합니다. 따라서 호이스팅도 없고, 변수를 읽으려는 시도에서는 ReferenceError 예외가 발생합니다. <br/><br/>

console.log(num); // ReferenceError <br/>
num = 6; // 초기화 <br/><br/>

다음은 호이스팅을 보이는 더 많은 예제입니다. <br/><br/>

// 예제 1 <br/>
// y만 호이스팅 대상 <br/><br/>

x = 1; // x 초기화. x를 선언하지 않은 경우 선언. 그러나 명령문에 var가 없으므로 호이스팅이 발생하지 않음 <br/>
console.log(x + " " + y); // '1 undefined' <br/>
// JavaScript는 선언만 호이스팅하므로, 윗줄의 y는 undefined <br/>
var y = 2; // y를 선언하고 초기화 <br/><br/>

// 예제 2 <br/>
// 호이스팅은 없지만, 변수 초기화는 (아직 하지 않은 경우) 변수 선언까지 병행하므로 변수를 사용할 수 있음 <br/><br/>

a = '크랜'; // a 초기화 <br/>
b = '베리'; // b 초기화 <br/><br/>

console.log(a + "" + b); // '크랜베리' <br/><br/>

- let과 const 호이스팅 <br/>
  let과 const로 선언한 변수도 호이스팅 대상이지만, var와 달리 호이스팅 시 undefined로 변수를 초기화하지는 않습니다. <br/>
  따라서 변수의 초기화를 수행하기 전에 읽는 코드가 먼저 나타나면 예외가 발생합니다. <br/><br/>

더 많은 정보는 let 문서의 "시간상 사각지대"를 참고하세요. <br/><br/>

console.log(a); <br/><br/>

var a = 10; <br/><br/>

console.log(a); <br/><br/>

//undefined <br/>
//10 <br/><br/>

## 클로져(closure)

클로져는 고급 주제 중 하나입니다. 관심이 있으시면 검색해서 공부해 보세요. <br/>
초급에서는 공부 안 해도 되는 주제이지만 중급에서는 꼭 알아야 하는 것 중 하나입니다. <br/>
참고링크 : https://developer.mozilla.org/ko/docs/Web/JavaScript/ Closures#%EC%96%B4%ED%9C%98%EC%A0%81*%EB%B2%94%EC%9C%84*%EC%A7%80%EC%A0%95lexical_scoping
