# 1일 TIL

- 간단하고 쉬운 python 문법으로 이루어진 문제를 20개 풀었다
- 근데? 문제를 풀다가 map 과 list 의 차이를 정확하게 몰라 어영부영 풀었지만 주변 팀원들의 도움으로 알게 되었다
  - map = (function, iterable)로 이루어져 있고 지연평가로 실제로 요소를 꺼낼 때 마다 함수가 적용
  - list = (iterable) 원소를 저장하는 컨테이너로 이것저것 가능

---

### iterable vs iterator

- iterable 이란?
  - 자료를 반복할 수 있는 객체로 흔히 쓰는 배열이 예시에 해당
- iterator 이란?
  - {value: 값, done: true/false} 형태의 이터레이터 객체를 리턴하는 메서드를 가진 객체

---

### 부동 소수점 float

- 부동 소수점(floating point) 방식은 소수점 (point) 이 둥둥 떠다닌다 (floating) 라는 의미로, 표현할 수 있는 값을 범위를 최대한 넓혀 오차를 줄이자는 시도에서 탄생한 녀석이다.
- 1.xxx X 2^n 으로 표현한다!!!!!!
