# 객체 2

- 객체는 유지 보수를 쉽게 하기 위해서 값들을 묶어 놓은 것으로, 속성과 메소드를 가집니다. <br/>
  var p1 = {"name": "honux", <br/>
  "eat": function(food) {}; <br/>
  }; <br/>

- 생성자로 여러 객체를 쉽게 만들기 <br/><br/>

비슷한 객체를 여러 개 만들 때는 객체를 생성하는 함수를 이용합니다. <br/>
이 때 객체를 생성하는 함수를 생성자라고 합니다. <br/>
생성자는 관례상 대문자로 시작하는 경우가 많습니다. <br/><br/>

//휴면 클래스를 정의하는 함수 = 생성자 <br/>
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
}; <br/>

- 생성자를 이용해서 객체 만들기 <br/><br/>

생성자를 이용해서 객체를 만들 때는 new 키워드를 사용합니다. <br/><br/>

var m1 = new Human("Honux", 100, 10); <br/>
var m2 = new Human("Crong", 999, 1); <br/>
m1.attack(m2); <br/>
m2.attack(m1); <br/>
m1.show(); <br/>
m2.show(); <br/><br/>

위 코드에서 m1은 객체 또는 인스턴스라고 합니다. <br/>
m1은 그리고 참조 변수입니다. 참조 변수에 대해서는 다음에.. <br/>

- 생성자를 사용하는 이유 <br/>
  객체를 하나만 만들 때는 간단히 json 표기법으로 만듭니다. <br/>
  여러 객체를 만들고 싶을 때는 생성자를 통해서 만듭니다. <br/>

## 예제

Food(name, energy) 생성자를 만들어 봅시다. <br/>
eat(food) 메소드를 Human() 생성자 안에 추가해 봅시다. <br/>
도너츠 객체를 생성해서 휴먼 객체에게 먹여 봅시다. <br/>

- 객체 조금 더 공부하기 <br/>
  https://opentutorials.org/course/743/6553
