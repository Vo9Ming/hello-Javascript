# 재귀의 기초2

## 점화식

- 재귀나 다이나믹 프로그래밍이라는 걸로 문제를 풀 때 유용하게 사용할 수 있는 수학 공식입니다.

## 재귀로 피보나치 수열 구현하기

- 피보나치 수열이란 오래 된 수학 문제 중 하나입니다.

## 피보나치 수열의 점화식

    f(0) = 0 f(1) = 1 f(n) = f(n-1) + f(n-2) f(0) = 0, f(1) = 1, f(2) = f(1) + f(0) = 1 + 0 = 1 f(3) = f(2) + f(1) = 1 + 1 = 2 f(4) = f(3) + f(2) 2 + 1 = 3

## 재귀로 피보나치 수열을 구현하기

1.  첫 번째 방법

    function fibo(n) {
    if (n <= 0) {
    return 0;
    }
    if (n == 1) {
    return 1;
    }
    return fibo(n - 1) + fibo(n - 2);
    }

2.  두 번째 방법 (옵션)

    var arr =[0, 1];

    function fibo_d(n) {
    if(arr[n] == undefined) {
    arr[n] = fibo_d(n - 1) + fibo_d(n - 2);
    }
    return arr[n];
    }

    이런 방법을 다이나믹 프로그래밍(또는 memoization) 기법이라고 합니다.
