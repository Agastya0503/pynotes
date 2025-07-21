---
title: Dsa Module
date: 2025-07-21
author: Your Name
cell_count: 22
score: 20
---

```python
#21072025
```


```python
from typing import List, Optional
```


```python
def linear_search(arr: List[int], target: int) -> int:
    for i, val in enumerate(arr):
        if val == target:
            return i
    return -1
```


```python
def binary_search(arr: List[int], target: int) -> int:
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
```


```python
  if arr[mid] == target:
            return mid
```


```python
elif arr[mid] < target:
            low = mid + 1
```


```python
else:
            high = mid - 1
    return -1
```


```python
def bubble_sort(arr: List[int]) -> List[int]:
    n = len(arr)
```


```python
for i in range(n):
        for j in range(n - i - 1):
```


```python
if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
    return arr
```


```python
def quick_sort(arr: List[int]) -> List[int]:
    if len(arr) <= 1:
        return arr
```


```python
 pivot = arr[0]
    left = quick_sort([x for x in arr[1:] if x <= pivot])
    right = quick_sort([x for x in arr[1:] if x > pivot])
    return left + [pivot] + right
```


```python
class Node:
    def __init__(self, data: int):
        self.data = data
        self.next: Optional['Node'] = None
```


```python
class LinkedList:
    def __init__(self):
        self.head: Optional[Node] = None
```


```python
def append(self, data: int):
        new_node = Node(data)
```


```python
if not self.head:
            self.head = new_node
    return
```


```python
temp = self.head
        while temp.next:
            temp = temp.next
        temp.next = new_node
```


```python
def display(self):
        elems = []
        temp = self.head
        while temp:
```


```python
 elems.append(str(temp.data))
            temp = temp.next
        print(" -> ".join(elems))
```


```python
 def search(self, key: int) -> bool:
        temp = self.head
        while temp:
```


```python
  if temp.data == key:
                return True
```


```python
 temp = temp.next
        return False
```


---
**Score: 20**