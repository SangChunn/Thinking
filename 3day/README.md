# 3일차 TIL

- 오늘은 SUNDAY 그래도 공부를 해야될 것 같아서 끄적끄적 했답니다.

- 복잡도 Big(O)
  ```
  버블정렬 : O(N^2) O(N^2) O(N^2)
  선택정렬 : O(N^2) O(N^2) O(N^2)
  삽입정렬 : O(N^2) O(N^2) O(N)
  쉘정렬   : O(N^1.5) O(N^2) O(N)
  퀵 정렬  : O(NlogN) O(N^2) O(NlogN)
  병합정렬 : O(NlogN) O(NlogN) O(NlogN)
              AVG      WORST   BEST
  ```
  - 선택정렬 : 정렬되지 않은 원소중 제일 작은 것을 정렬된 곳 맨 앞에다가 넣어버리는 것
  - 삽입정렬
    - 두 번째 원소부터 확인하면서 앞쪽에 삽입
    - 정렬되지 않은 부분에서 뽑은 뒤 앞쪽으로 넣고 크기 확인하면서 위치 조절
  - 퀵정렬
    - pivot 하나 선택 거의 중간?
    - 피벗을 중심으로 왼쪽은 오른쪽으로 이동하면서 pivot보다 커지는 상황 전까지 이동 오른쪽은 반대로
    - 그 후 두 지점이 멈추면 교환 그 후 pl과 pr이 교차되거나 만날때 까지 진행
    - 그 후 가운데를 나눠 다시 진행
  - 병합정렬
    - 부분 리스트의 사이즈가 1이 될때 까지 분할!!!!
    - 그 후 2개씩 합쳐서 정렬 후 2-2 합쳐서 정렬 무한반복

---

- python permutations

  ```
  from itertools import permutations

  arr = [1, 2, 3]
  for p in permutations(arr, 2):
      print(p)
      (1, 2), (1, 3), (2, 1), (2, 3), (3, 1), (3, 2)
  ```

  - `permutations(iterable, r)`의 **입력**: 리스트/튜플/문자열/range 등 “반복가능 객체”
  - **산출(요소)**: **튜플(tuple)**입니다. 길이는 `r`(생략 시 `len(iterable)`).

    - 즉, `for p in permutations(A, N):`에서 `p`는 `A`의 원소로 이루어진 **길이 N짜리 튜플**이에요.
