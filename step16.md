# 객체와 프로토타입

## prototype

- 생성자로 만든 객체는 프로토타입이라는 속성을 가집니다. <br/>
  자바스크립트로 객체 지향 프로그래밍을 하기 위해서는 프로토타입을 잘 이해해야 합니다. <br/><br/>

일단 우리는 프로토타입을 이용해서 메소드를 생성하려 합니다. <br/>
이렇게 하면 메모리를 절약하고 효율적으로 객체의 메소드를 생성할 수 있습니다. <br/><br/>

function Human(name, hp, mp, power) { <br/>
this.name = name; //m1.name = name; <br/>
this.hp = hp; <br/>
this.mp = mp; <br/>
this.power = power; <br/>
}<br/><br/>

Human.prototype.attack = function(target) { <br/>
target.hp -= this.power; <br/>
}; <br/><br/>

===================================================================
전에 배웠던 것과 비교해보기. <br/><br/>

var Human = function(name, hp, power) { <br/>
this.name = name; <br/>
this.hp = hp; <br/>
this.power = power; <br/>
this.attack = function(target) { <br/>
target.hp -= this.power; <br/>
}; <br/>
this.show = function() { <br/>
console.log("%s %d %d %d", <br/>
this.name, this.hp, this.mp, this.power); <br/>
}; <br/>
}; <br/><br/>

## 배열과 객체

- 객체의 속성값이 배열이 될 수 있습니다. 배열 안에 값들이 객체가 될 수 있습니다. <br/>
  var m1 = {'no': 1, 'scores': [100, 99]}; <br/>
  var m2 = {'no': 2, 'scores': [100, 99]}; <br/>
  var arr1 = [m1, m2]; <br/><br/>

## 배열, 객체와 참조변수

=> 객체를 변수에 할당하면 그 변수는 참조 변수가 됩니다. 배열도 객체이므로 배열을 변수에 할당하면 역시 참조 변수가 됩니다. <br/>
함수 호출시 참조 변수를 매개 변수로 전달하면 함수 내부에서 변경한 값이 외부에서도 변경된다는 것 꼭 기억하세요. <br/>
