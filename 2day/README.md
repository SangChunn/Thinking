# 2일차 TIL

- 아침엔 백준을 풀어보자고 생각해서 백준을 풀었당!!! 그중에서 어려웠다고 생각하는 것들과 좀 배워간 것들? 적어보겠습니다
- 에라토스테네스의 채

  ```
  def primenum(n):
  prime = [True] * (n + 1)
  prime[0] = prime[1] = False

  for i in range(2, int(n**0.5) + 1):
      if prime[i]:
          for j in range(i * i, n + 1, i):
              prime[j] = False
  return prime
  ```

  먼저 prime[0]과 prime[1]은 소수가 아니기 때문에 False로 설정하고 sqrt()로 소수를 구하면 된다!

- for 문
  ```
  for i in range(a, b, c)
      -> 시작지점 a, b는 끝나는 지점, c는 증가/감소율
  ```
  ```
  marks = [90, 25, 67, 45]
  for i in marks:
    -> marks 안 요소들을 i가 돌면서 확인
    print(i)
    90
    25
    67
    45
  순차적으로 하나씩 출력
  len() 사용하면 굿
  ```
  ```
  만약 cut_list = [list(map(int, (input().split()))) for _ in range(num)]
  이렇게 list [[a,b],
  					[c,d]] 2차원 배열로 가져오면
  for i, j in cut_list:
    i는 앞쪽 j는 뒤를 가르킴
  ```
- 재귀함수들
  ```
  def factroial(n):
    if n > 0:
  	    return n * factorial(n-1)
    else:
  	    return 1
  ```
  ```
  def hanoi(n, x, y, z):
  if n == 1:
  	return (x, z)
  else:
  	hanoi(n-1, x, z, y)
  	return (x, z)
  	hanoi(n-1, y, x, z)

  total = 2^n- 1
  ```
- GCD, LCM
  ```
  def gcd(x, y):
  if y == 0 :
  	return x
  else:
  	return gcd(y, x%y)
      (x가 y보다 크다 라는 전제조건 필수)
  ```

---

## 아!!!!! 내일은 복잡도 조금!! 보고 완전탐색을 살짜아악 볼거다!!!
