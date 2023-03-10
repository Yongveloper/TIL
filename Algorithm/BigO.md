# 빅오(Big-O) 표기법이란?

> 입력값과 연산 수행 시간에서 상관관계를 나타내는 척도를 시간 복잡도라고 하고 이를 빅오(Big O) 표기법으로 표기한다. 물론 공간 복잡도에 대해서도 사용될 수 있다.
> 입력된 값이 커질수록 알고리즘 실행시간이 어떻게 변하는지 설명하는 공식적인 방법.
> 시간 복잡도, 공간 복잡도를 쉽게 볼 수 있게 표기하는 대표적인 방법 빅오(Big O)다.

## 💡 빅오(Big-O) 표기 방법

몇 가지 예시를 들어 본다.

### 1. <code>O(1)</code>

```javascript
function addUpTo2(n) {
  return (n * (n + 1)) / 2;
}
```

입력값 n이 커질수록 약간의 변동을 있을 수 있지만 전반적인 주제에는 변화가 없다.

10으로 계산하던지 10000으로 계산하던지 연산하는 수(코드에서의 곱셉, 덧셈, 나눗셈)는 변하지 않기 때문에

<code>O(1)</code>로 표기한다.

## 2. <code>O(n)</code>

```javascript
function addUpTo(n) {
  let total = 0;
  for (let i = 1; i <= n; i++) {
    total += i;
  }
  return total;
}
```

반복문을 사용하기 때문에 입력값 n이 커질수록 연산을 하는 횟수는 n의 크기에 따라서 변하게 된다.

반복문에서 보면 i와 n을 비교하고, i를 증가시키고, 변수 total에 더해주고 하고 있는데,

n이 10이면 이 연산들을 10번 더 반복하게 되는 것이고 10,000번이면 이 연산들을 10,000번 더 반복하게 된다.

n의 크기에 따라서 시간이 달라지게 되기 때문에 O(n)으로 표기한다.

빅오(Big O)는 디테일한 것은 신경 쓰지 않고 광범위한 부분만 보면 된다.

즉, 광범위한 추세만 보기에는 상수는 전혀 중요하지 않기 때문에 O(10n) => O(n), O(300) => O(1), O(5n^2) => O(n^2) 등 이런 식으로 표기하는 것이다.

### 계산방법?

간단하게 말하면 연산이 몇 번 수행되는지, 입력 값과 연산의 관계가 어떻게 되는지 보면 쉽게 알 수 있다.

## 💡빅오(Big-O) 표기법의 종류

<code>O(1)</code>: 입력값이 크기에 많은 차이가 있어도 일정한 실행시간을 보여주는 최고의 알고리즘이라고 할 수 있다.

<code>O(log n)</code>: 로그는 입력값이 매우 커도 크게 영향을 받지 않는 알고리즘에 해당된다.

<code>O(n)</code>: 입력값과 알고리즘 수행시간이 비례한다.

<code>O(n log n)</code>: 병합 정렬 같은 효율이 좋은 알고리즘이 대부분 이에 해당된다.

<code>O(n^2)</code>: 중첩, 버블 정렬 같은 비 효율적인 알고리즘이다.

<code>O(2^n)</code>: 피보나치의 수를 재귀함수로 계산하는 알고리즘에 해당된다.

<code>O(n!)</code>: 매우 느리고 입력값이 작아도 계산 속도가 매우 증가한다.

<img src="https://user-images.githubusercontent.com/64254228/212916956-13deb47f-328f-407c-ad65-accd6af04806.png" width="450px" height="300px" title="BigO시간복잡도" alt="시간복잡도 표"></img><br/>

<img src="https://user-images.githubusercontent.com/64254228/212917061-595fe003-0674-42a7-b9c4-d50ae4a52350.png" width="450px" height="300px" title="BigO시간복잡도" alt="시간복잡도 표"></img>

## 💡배열 메소드 Big-O

<img src="https://user-images.githubusercontent.com/64254228/212918496-f4c9c4bb-4379-4a89-8c2d-e3b4a4b91cda.png" width="450px" height="300px" title="BigO시간복잡도" alt="시간복잡도 표"></img>
