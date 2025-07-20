---
title: Dsa
date: 2025-07-21
author: Your Name
cell_count: 45
score: 45
---

```python
#21072025
```


```python
class Stack:
    def __init__(self):
        self.items = []

    def push(self, item):
        print(f"Pushed {item} to stack.")
        self.items.append(item)

    def pop(self):
        if not self.is_empty():
```


```python
print(f"Popped {self.items[-1]} from stack.")
            return self.items.pop()
```


```python
 print("Stack is empty.")
        return None
```


```python
def peek(self):
        return self.items[-1] if not self.is_empty() else None

    def is_empty(self):
        return len(self.items) == 0

    def display(self):
```


```python
  print("Stack:", self.items)
```


```python
class Queue:
    def __init__(self):
        self.items = []

    def enqueue(self, item):
        print(f"Enqueued {item} to queue.")
        self.items.insert(0, item)

    def dequeue(self):
        if not self.is_empty():
```


```python
print(f"Dequeued {self.items[-1]} from queue.")
return self.items.pop()
```


```python
print("Queue is empty.")
        return None
```


```python
  def is_empty(self):
        return len(self.items) == 0
```


```python
def display(self):
        print("Queue:", list(reversed(self.items)))
```


```python
class Queue:
    def __init__(self):
        self.items = []
```


```python
def enqueue(self, item):
        print(f"Enqueued {item} to queue.")
        self.items.insert(0, item)
```


```python
def dequeue(self):
        if not self.is_empty():
```


```python
print(f"Dequeued {self.items[-1]} from queue.")
```


```python
return self.items.pop()
```


```python
print("Queue is empty.")
```


```python
return None
```


```python
 def is_empty(self):
        return len(self.items) == 0
    def display(self):
```


```python
print("Queue:", list(reversed(self.items)))
```


```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
```


```python
class LinkedList:
    def __init__(self):
        self.head = None
```


```python
  def insert_end(self, data):
```


```python
print(f"Inserted {data} into linked list.")
```


```python
new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        last = self.head
        while last.next:
            last = last.next
        last.next = new_node
```


```python
 def display(self):
        temp = self.head
```


```python
 print("Linked List: ", end='')
while temp:
```


```python
 print(temp.data, end=" -> ")
```


```python
temp = temp.next
        print("None")
```


```python
def bubble_sort(arr):
    print(f"Original Array: {arr}")
```


```python
n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
```


```python
  print(f"Swapped {arr[j]} and {arr[j+1]}")
```


```python
arr[j], arr[j+1] = arr[j+1], arr[j]
    print(f"Sorted Array: {arr}")
    return arr
```


```python
def binary_search(arr, target):
    print(f"Searching for {target} in {arr}")
    low = 0
    high = len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
```


```python
            print(f"Found {target} at index {mid}")
```


```python
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    print(f"{target} not found.")
    return -1
```


```python
def dfs(graph, node, visited=None):
    if visited is None:
        visited = set()
    if node not in visited:
```


```python
print(node, end=' ')
```


```python
        visited.add(node)
        for neighbor in graph[node]:
            dfs(graph, neighbor, visited)
```


```python
def menu():
    print("\n--- DSA MENU ---")
    print("1. Stack Demo")
    print("2. Queue Demo")
    print("3. Linked List Demo")
    print("4. Bubble Sort")
    print("5. Binary Search")
    print("6. DFS Graph Traversal")
    print("0. Exit")
```


```python
if __name__ == "__main__":
    while True:
        menu()
        choice = input("Enter choice: ")
```


```python
 print("DFS Traversal:")
            dfs(graph, 'A')
            print()
```


```python
  elif choice == '0':
            print("Exiting...")
            break
```


```python
 else:
            print("❌ Invalid choice. Try again.")
```


```python

```


---
**Score: 45**