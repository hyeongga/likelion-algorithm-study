# 개념정리
> 스택과 큐를 사용할 때는 삽입과 삭제 외에도 `오버플로`와 `언더플로`를 고민해야한다.<br>
`오버플로`는 특정한 자료구조가 수용할 수 있는 데이터의 크기를 이미 가득찬 상태에서 삽입 연산을 수행할 때 발생한다. 즉 저장 공간을 벗어나 데이터가 넘쳐흐를 때 발생한다.<br>
반면에 특정한 자료구조에 데이터가 전혀 들어 있지 않은 상태에서 삭제 연산을 수행하면 데이터가 전혀 없는 상태이므로 `언더플로`가 발생한다.<br>

## 스택
> 스택은 박스 쌓기에 비유할 수 있다. 박스는 아래에서 위로 차곡차곡 쌓는데, 아래에 있는 박스를 치우기 위해서는 위에 있는 박스 먼저 내려야 하기 때문이다.<br>
이러한 구조를 `선입후출`, `후입선출` 이라고 한다.

--- 

# 문제 풀이

---
## <이것이 코딩 테스트다.>
### 예제 5-1
```
stack = []

stack.append(5)
stack.append(2)
stack.append(3)
stack.append(7)
stack.pop()
stack.append(1)
stack.append(4)
stack.pop()

print(stack) # 최하단 원소부터 출력
print(stack[::-1]) # 최상단 원소부터 출력
```

> 파이썬에서 스택을 이용할 때에는 라이브러리를 사용할 필요가 없다.<br>
기본 리스트에서 append()와 pop() 메서드를 이용하면 스택 자료구조와 동일하게 작업을 수행할 수 있다.

---
---

## 큐
> 큐는 대기 줄에 비유할 수 있다.<br>
먼저 들어간 사람이 먼저 나오는 구조로 `선입선출` 구조라고 한다.

---

# 문제 풀이

---
## <이것이 코딩 테스트다.>
### 예제 5-2
```
from collections import deque

# 큐 구현을 위해 deque 라이브러리 사용
queue = deque()

queue.append(5)
queue.append(2)
queue.append(3)
queue.append(7)
queue.popleft()
queue.append(1)
queue.append(4)
queue.popleft()

print(queue) # 먼저 들어온 순서대로 출력
queue.reverse() # 다음 출력을 위해 역순으로 변경
print(queue) # 나중에 들어온 원소부터 출력
```


