# 재귀의 기초

## 재귀란?

- 함수가 함수 안에서 자신을 다시 호출하는 것
  var foo = function() {
  foo();
  }

## 카운트다운 재귀로 구현하기

- 카운트 다운 일반 버전

  var countdown = function(n) {
  for (var i = n; i >= 0; i--) {
  console.log(i);
  }
  };

  countdown(10);

- 재귀로 구현하기 1

  var countdown2 = function(n) {
  console.log(n);
  countdown2(n - 1);
  };
  위 코드는 종료 조건이 빠져 있기 때문에 무한 루프처럼 종료가 되지 않습니다!
  재귀 함수는 반드시 종료 조건이 필요합니다!

- 재귀 함수에 종료 조건 추가

  var countdown2 = function(n) {

        //termination condition

        console.log(n);
        if (n <= 0) {
            return;
        }

        countdown2(n - 1);

  };

  \* 재귀에는 반드시 종료조건이 필요하다.

## 왜 재귀를 사용하나?

- 재귀를 사용하면 쉽게 풀리는 문제들이 많이 존재하기 때문입니다.
- 예를 들어, 알고리즘의 리스트, 트리, 그래프 순회 문제는 재귀로 푸는 게 편합니다.

## 재귀 vs 일반

- 일반 함수가 재귀 함수보다 높은 성능을 보인다.
- 모든 재귀 알고리즘은 일반 알고리즘으로 바꿀 수 있다.

## 그런데 왜?

재귀 없이 구현하면 성능이 좋아지고 재귀를 사용하면 프로그래머의 능력이 좋아집니다.

## 재귀로 구현하기 연습

- a부터 b까지 정수를 더해서 리턴해 주는 함수
  var rsum = function(a, b) {
  if (a == b) {
  return a;
  }
  return b + rsum(a, b - 1);
  }

  var x = rsum(1, 10);
  console.log(x);

## 재귀로 팩토리얼 구현하기

    fact(3) = 3 _ 2 _ 1
    var fact = function(n) {
    //implement
    };
