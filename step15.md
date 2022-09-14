# 참조 변수와 Call by Reference

### 값에 의한 전달 이해하기

- 참조 변수와 일반 변수 <br/>
  : 객체를 변수에 할당하면 참조 변수가 되고, 기본 타입을 변수에 할당하면 일반 변수가 됩니다. <br/><br/>

- 일반 변수에서 값 복사 및 바꾸기 <br/>
  : 일반 변수는 값만 저장하고 다른 변수에 언제나 독립적으로 존재합니다. <br/>
  var a = 5; <br/>
  var b = a; <br/>
  a === b (true) <br/>
  b = 10 <br/>
  a === b (false) <br/>
  위 코드에서 a와 b는 처음에는 값이 같으나 사실은 다른 변수이다. <br/><br/>

- 참조 변수의 동작 방식 이해하기 <br/>
  : 참조 변수라는 것은 객체에 대한 별명 같은 것입니다. <br/>
  같은 사람을 이름으로도 부르고 별명으로도 부르는 것처럼 <br/>
  다양한 호칭으로 부르는 것과 비슷한 개념이라고 생각하면 된다. <br/>
  객체를 만들면 객체가 생기고 변수에는 그 객체의 참조를 할당하는 것. <br/>
  var m1 = {name : "honux", age : 25}; <br/>
  var m2 = m1; <br/>
  m1 === m2; (true) <br/>
  m2.name = "crong"; <br/>
  m1; ({name : 'crong', age : 25}) <br/>
  m1 === m2; (true) <br/><br/>

  !!!일반 변수와는 전혀 다른 결과가 나옴을 알 수 있다. 차이점 잘 캐치해두기!!! <br/><br/>

- 함수 호출시의 변수 \_ 두 코드의 동작되는 차이에 주목! <br/>
  => 값 전달 <br/>
  var foo_v = function(v){ <br/>
  v = v \* 2; <br/>
  console.log(v); <br/>
  } <br/><br/>

  var a = 10; <br/>
  foo_v(a); (20) <br/>
  console.log(a); (10) <br/><br/>

  => 참조 전달 <br/>
  var foo_r = function(ref){ <br/>
  ref.v = ref.v \* 2; <br/>
  console.log(ref); <br/>
  } <br/><br/>

  var p = {name : "Dora", v : 99}; <br/>
  foo_r(p); ({name : "Dora", v : 198}) <br/>
  console.log(p); ({name : "Dora", v : 198}) <br/><br/>

===> 즉, 값 전달 변수(일반 변수)는 함수 내부에서 값을 바꿔도 외부에서는 그대로이지만, <br/>
참조 전달 변수(참조 변수)는 함수 내부에서 값을 바꾸면 외부의 객체도 값이 바뀐다. <br/>
