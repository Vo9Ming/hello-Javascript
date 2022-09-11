# 배열과 문자열 2

# 배열과 문자열의 메소드 살펴보기

## 복습

- Array (배열, 어레이) - 여러 데이터를 담을 수 있는 자료구조이다.
- 자바스크립트에서 배열은 객체이므로 속성과 메소드를 가진다.
- 배열과 문자열은 유사하다.
- 배열은 mutable, 문자열은 immutable 특징이 있다.
- 속성: length(문자열의 길이)
- 메소드: push()* 맨뒤에 넣는거, pop()*맨뒤에서 뻬오는거, unshift()*맨 앞에 넣는것, shift()*맨 앞에서 빼오는 것

# 배열의 메소드 더 살펴보기

- concat() : concat: 배열 합치기, 문자열도 가능 <br/><br/>

- join() : 배열을 문자열로 바꿀 때 사용합니다. <br/><br/>

- indexOf(), lastIndexOf() : 배열이나 문자열안의 원소를 가지고 인덱스를 찾을 수 있음 <br/>
  var a = [10, 20, 30, 40, 10, 50]; <br/>
  a.indexOf(10); <br/>
  a.indexOf(65535); <br/>
  a.lastIndexOf(10); <br/><br/>

- slice() <br/>
  사용법: slice(startIndex, endIndex) 기존 배열을 잘라서 새로운 배열을 만든다. <br/>
  기존 배열은 변하지 않는다. <br/>
  startIndex 위치부터 endIndex 직전의 위치까지 자릅니다. endIndex의 원소는 포함되지 않는다. <br/><br/>
  a = [1, 2, 3, 4, 5]; <br/>
  a.slice(2, 4); <br/>
  a; <br/>

- splice() <br/>
  사용법: splice(startIndex, numElement) <br/>
  배열을 startIndex부터 numElement 개수만큼 잘라낸다. <br/>
  잘라낸 원소들은 원본 배열에서 사라집니다. <br/><br/>

\*\* slice()와 splice()는 둘다 유용하므로 각각의 사용법을 잘 기억해 놓는 게 좋습니다. <br/>

- 문자열의 split() <br/>
  문자열을 문자의 배열로 나누고 싶을 때 사용하는 메소드. <br/>
  var s = "hello, world a-b-co,ltd";<br/>
  s.split(""); <br/>
  s.split(","); <br/>
  s.split("-"); <br/>
