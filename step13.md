# 조건문 2 : switch-case

- 변수에 저장된 값에 따라 각각 다른 코드를 실행하는 분기문입니다.
  상황에 따라 if 와 else if를 반복적으로 써야 하는 상황을 피하게 해 줍니다.

## 문법

<br/>
var value; <br/>
switch(value) { <br/>
    case 값1: <br/>
    //value == 값1일 경우 실행할 코드 <br/>
    break; <br/>
    case 값2: <br/>
    //value == 값2일 경우 실행할 코드 <br/>
    break; <br/>
    //... <br/>
    default: <br/>
    //위쪽에 해당되지 않는 경우 실행할 코드 <br/>
} <br/>

## 예제

- 점수가 10점이면 A, 9점이면 B, 그 외에는 C를 출력하는 코드를 작성하세요. <br/>

### if로 구현

<br/>
var score = prompt('점수를 입력하세요'); <br/>
if (score === 10) { <br/>
    console.log('A'); <br/>
} else if (score == 9) { <br/>
    console.log('B'); <br/>
} else { <br/>
    console.log('C'); <br/>
} <br/>

### switch-case 로 구현

<br/>
var score = prompt('점수를 입력하세요'); <br/>
switch (score) { <br/>
    case 10: <br/>
    console.log('A); <br/>
    break; <br/>
    case 9: <br/>
    console.log('B'); <br/>
    break; <br/>
    default: <br/>
    console.log('C'); <br/>
} <br/>
