---
title: Pynotes Dsa Trainer
date: 2025-07-21
author: Your Name
cell_count: 57
score: 55
---

```python
#21072025
```


```python
from typing import List, Optional
```


```python
def linear_search(arr: List[int], target: int) -> int:
    print("\n Starting Linear Search")
```


```python
 for i, val in enumerate(arr):
        print(f"Checking index {i} → {val}")
```


```python
if val == target:
            print(f"✅ Found {target} at index {i}")
```


```python
            return i
    print(f" {target} not found in the list.")
    return -1
```


```python
def binary_search(arr: List[int], target: int) -> int:
    print("\n Starting Binary Search")
```


```python
 arr.sort()
    print(f"Sorted array: {arr}")
```


```python
 low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        print(f"Checking middle index {mid} → {arr[mid]}")
```


```python
 if arr[mid] == target:
            print(f" Found {target} at index {mid}")
```


```python
return mid
        elif arr[mid] < target:
            print(f"{arr[mid]} < {target}, moving right")
```


```python
  low = mid + 1
        else:
```


```python
 print(f"{arr[mid]} > {target}, moving left")
            high = mid - 1
```


```python
    print(f" {target} not found.")
    return -1
```


```python
def bubble_sort(arr: List[int]) -> List[int]:
    print("\n Starting Bubble Sort")
```


```python
 n = len(arr)
    for i in range(n):
```


```python
print(f"Pass {i + 1}")
        for j in range(n - i - 1):
```


```python
 print(f"Comparing {arr[j]} and {arr[j + 1]}")
            if arr[j] > arr[j + 1]:
```


```python
print(f"Swapping {arr[j]} ↔ {arr[j + 1]}")
arr[j], arr[j + 1] = arr[j + 1], arr[j]

```


```python
print(f"Array after pass {i + 1}: {arr}")
print(f"Sorted array: {arr}")
```


```python
return arr
def quick_sort(arr: List[int]) -> List[int]:
    if len(arr) <= 1:
        return arr
    pivot = arr[0]
```


```python
 print(f"\n Quick Sort Pivot: {pivot}")
```


```python
left = [x for x in arr[1:] if x <= pivot]
right = [x for x in arr[1:] if x > pivot]
```


```python
print(f"Left: {left} | Right: {right}")
return quick_sort(left) + [pivot] + quick_sort(right)
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
        print(f" Appending {data} to linked list.")
```


```python
  new_node = Node(data)
        if not self.head:
            self.head = new_node
            print(f"Head initialized with {data}")
```


```python
  return
        temp = self.head
        while temp.next:
            temp = temp.next
        temp.next = new_node
        print(f"{data} appended at the end.")
```


```python
  def display(self):
        print(" Linked List:")
        elems = []
        temp = self.head
        while temp:
            elems.append(str(temp.data))
            temp = temp.next
        print(" -> ".join(elems))
```


```python
def search(self, key: int) -> bool:
print(f" Searching {key} in Linked List")
```


```python
temp = self.head
while temp:
```


```python
print(f"Checking node with value {temp.data}")
```


```python
if temp.data == key:
                print(f" Found {key}")
```


```python
  return True
            temp = temp.next
        print(f" {key} not found.")
        return False
```


```python
def run_quiz():
    print("\n Welcome to DSA Quiz Mode")
    questions = [
```


```python
{
  "question": "Which sorting algorithm is best for nearly sorted data?",
  "options": ["A. Quick Sort", "B. Merge Sort", "C. Insertion Sort", "D. Heap Sort"],
  "answer": "C"
 },
```


```python
 {
"question": "What is the time complexity of Binary Search?",
"options": ["A. O(n)", "B. O(log n)", "C. O(n log n)", "D. O(1)"],
 "answer": "B"
 },
```


```python
{
"question": "Which data structure uses FIFO?",
"options": ["A. Stack", "B. Queue", "C. Tree", "D. Graph"],
"answer": "B"
}
]
```


```python
score = 0
    for i, q in enumerate(questions):
        print(f"\nQ{i + 1}: {q['question']}")
```


```python
for opt in q['options']:
            print(opt)
```


```python
ans = input("Your answer (A/B/C/D): ").strip().upper()
        if ans == q["answer"]:
            print(" Correct!")
```


```python
 score += 1
        else:
            print(f" Wrong. Correct answer: {q['answer']}")
```


```python
 print(f"\n🎉 Final Score: {score}/{len(questions)}")
```


```python
def main_menu():
    ll = LinkedList()
    while True:
        print("\n PyNotes DSA Trainer Menu")
        print("1. Linear Search")
        print("2. Binary Search")
        print("3. Bubble Sort")
        print("4. Quick Sort")
        print("5. Linked List (Append/Search/Display)")
        print("6. DSA Quiz Mode")
        print("0. Exit")
```


```python
 choice = input("Choose an option: ")

        if choice == '1':
            arr = [int(x) for x in input("Enter list of numbers: ").split()]
            target = int(input("Enter value to search: "))
            linear_search(arr, target)
```


```python
elif choice == '2':
            arr = [int(x) for x in input("Enter sorted list: ").split()]
            target = int(input("Enter value to search: "))
            binary_search(arr, target)

```


```python
 elif choice == '3':
            arr = [int(x) for x in input("Enter list: ").split()]
            bubble_sort(arr)
```


```python
elif choice == '4':
            arr = [int(x) for x in input("Enter list: ").split()]
            print(f"Before: {arr}")
            sorted_arr = quick_sort(arr)
            print(f"After Quick Sort: {sorted_arr}")
```


```python
elif choice == '5':
            while True:
                print("\nLinked List Menu")
                print("a. Append")
                print("b. Search")
                print("c. Display")
                print("d. Back to main menu")
```


```python
sub = input("Choose an option: ")
                if sub == 'a':
                    val = int(input("Enter value to append: "))
                    ll.append(val)
```


```python
lif sub == 'b':
                    val = int(input("Enter value to search: "))
                    ll.search(val)
                elif sub == 'c':
                    ll.display()
                elif sub == 'd':
```


```python
 break
                else:
                    print(" Invalid option.")
```


```python
  elif choice == '6':
            run_quiz()
```


```python
elif choice == '0':
            print(" Exiting PyNotes DSA Trainer. Goodbye!")
            break

```


```python
 else:
            print(" Invalid choice. Please select a valid option.")
```


```python
if __name__ == "__main__":
    main_menu()
```


---
**Score: 55**