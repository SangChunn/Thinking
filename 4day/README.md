# 4일차 TIL

- 아 CS 좀 어렵다. 머리아프다. 졸리다. 배워갈게 많긴 하네. 한번 적어볼까?

---

- CPU가 ALU 입장에서 어떻게 하냐
  - 4가지로 나뉜다. Fetch, Decode, Execute, Writeback
    - Fetch : CPU가 주기억 장치에서 명령어를 가져온다
    - Decode : 명령어를 해석
    - Execute : 명령어 실행
    - WirteBack : 메모리에 적재
- OS의 가상화 3가지
  - Processes
  - Virtual memory
  - Files
- OS왜 쓰는지 2가지
  - 제멋대로 동작하는 응용프로그램들이 하드웨어를 잘못 사용하는 것을 막기 위해
  - 응용프로그램들이 단순하고 균일한 메커니즘을 사용해 복잡하고 저수준 하드웨어 장치 조작
- Cache 란?
  - 데이터를 register로 가져올 때 빠르게 가져오기 위해서 !!
  - locality 로 더 빨라짐
  - 순서는 Register(L0), L1, L2, L3, MainMemory, LD(local disk)
- hello.c -> 전처리 -> hello.i -> 컴파일러 -> hello.s -> 어셈블러 -> hello.o -> Linker -> 실행파일
  - 전처리 단계 : 헤더파일을 저장
  - 컴파일러 : 어셈블리어 언어로 바꿔줌
  - 어셈블러 : 기계어로 변환
  - 링커 : 모든 코드들을 실행파일 하나로 묶어버림

---

- Quick sort
  ```
  def quick_sort(arr): # 원소가 1개 이하일 경우 그대로 반환
  if len(arr) <= 1:
  return arr

      # 피벗: 리스트의 첫 번째 원소
      pivot = arr[0]    (원래는 pivot 중간값으로 해야됨 ㅇㅇㅇㅇㅇㅇ)

      # 피벗 기준으로 작은 값과 큰 값 나누기
      left = [x for x in arr[1:] if x <= pivot]
      right = [x for x in arr[1:] if x > pivot]

      # 재귀적으로 정렬 후 합치기
      return quick_sort(left) + [pivot] + quick_sort(right)
      ```
