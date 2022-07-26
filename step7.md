# 반복문 2. 

## break 와 continue
- break는 반복문을 중간에 빠져나갈 때 사용합니다. 
- 무한 루프와 함께 많이 사용합니다. <br/><br/><br/>

var str;<br/>
while (true) {<br/>    
    str = prompt("아무거나 입력하세요");<br/>
    document.write(str + "<br>");<br/>
    if (str == "q") {<br/>
        break;<br/>
    }<br/>
}<br/>
document.write("Bye~");<br/><br/>

### 아래 코드의 실행 결과를 예측해 보세요.
for(var i = 0;i < 10; i++) { <br/>
    if (i == 5) {  <br/>
        break; <br/>
    } <br/>
    console.log(i); <br/>
} <br/><br/>
 0 1 2 3 4  <br/>
 break를 만나는 순간 for문에서 빠져나온다.<br/>
 break는 반복문 한개, 루프 한개만 빠져나온다.<br/>


## continue는 반복문의 처음으로 돌아갑니다. (빠져나가는 것이 아님. 루프의 처음으로 돌아간다.)
* while: 조건식( i < 10 )으로 이동
* for: 증감식 ( i++) 으로 이동 <br/><br/><br/>

for(var i = 0;i < 10; i++) { <br/>
    if (i == 5) { <br/>
        continue; <br/>
    } <br/>
    console.log(i); <br/>
} <br/><br/><br/>

0, 1, 2, 3, 4, 6, 7, 8, 9 <br/>
i === 5 일때는 continue 를 만나면 console.log(i)를 가지않고 바로 i++로 간다.<br/><br/>




## 이중 루프
- 반복문 안에 반복문이 있는 걸 이중 루프라고 합니다. 
- 종종 사용한다. 3중, 4중도 가능하지만 잘 사용하지 않는다. <br/><br/>

for (var i = 0; i < 2; i++) { <br/>
    for (var j = 0; j < 3; j++) { <br/>
        console.log(i + ", " +j); <br/>
    } <br/>
} <br/><br/>
 (0,0), (0,1), (0,2)
 (1,0), (1,1), (1,2)

## (생각해 보기) 이중 루프 중간에 한꺼번에 빠져나갈 수 있을까? 
for (var i = 0; i < 3; i++) { <br/>
    for (var j = 0; j < 5; j++) { <br/>
        console.log("i= " + i+ ", j= " + j); <br/>
        if (j == 2) {<br/>
            break;<br/>
        }<br/>
    }<br/>
}<br/><br/><br/>

 i = 0, j = 0 <br/>
 i = 0, j = 1 <br/>
 i = 0, j = 2 <br/>
 i = 1, j = 0 <br/>
 i = 1, j = 1 <br/>
 i = 1, j = 2 <br/>
 i = 2, j = 0 <br/>
 i = 2, j = 1 <br/>
 i = 2, j = 2 <br/>