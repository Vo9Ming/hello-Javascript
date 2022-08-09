# 객체1.객체의 기초

## 객체란 무엇인가?
- 현실의 물체에 대응되는 개념입니다.
- 객체를 사용하면 변수와 함수를 묶어서 관리하게 됩니다.
- 객체는 속성과 메소드를 가집니다.


## 객체 만들기
p1 = {}; <br/>


###  속성
- 객체에 속한 변수 <br/>
p1.name = "Hoyoung Jung"; <br/>
console.log(p1.name); <br/> 

### 메소드

- 객체에 속한 함수
p1.eat = function(food) { <br/>
    console.log(this.name + " ate delicious " + food +"..."); <br/>
}; <br/>

p1.eat("Beef"); <br/>           
==> Hoyoung Jung ate delicious Beef... 이 도출됨


### 메소드 대신에 일반 함수를 썼다면?
eat(p1, "Beef"); <br/>
==> VM407:1 Uncaught ReferenceError: eat is not defined <br/>
    at <anonymous>:1:1 <br/>


## 객체 지향 프로그래밍
- 유지보수가 쉬워진다.
- 가독성이 높아진다.
- 대형 프로그램을 짜기 쉬워진다.


## 객체 지향 프로그래밍
- 객체와 객체가 협력해서 일을 한다.
- 객체는 일에 책임을 진다.
- 객체는 객체에 메시지를 보낸다.
- 객체는 자율적으로 일을 한다.


## this 키워드
- 메소드 안에서 사용시 함수를 소유한 객체를 가르킨다.
var p2 = {}; <br/>
p2.name = "crong"; <br/>
p2.weight = 80; <br/>
p2.say = function(word) { <br/>
    console.log(this.name + " says, " + word); <br/>
}; <br/>


## 객체 만들기2
- JSON 표기법을 이용해서 객체를 만들 수도 있습니다. 생성자 함수를 이용하는 방법도 있지만 다음에 ... <br/>
var m1 = { <br/>
  "name": "Honux", <br/>
  "hp": 100, <br/>
  "power": 10, <br/>
  "attack": function(target) { <br/>
    target.hp -= this.power; <br/>
  } <br/>
}; <br/><br/>

var c1 = { <br/>
   type: "Coffee", <br/>
   energy: 10 <br/>
}; <br/> <br/>

//m1.eat(c1); <br/>
