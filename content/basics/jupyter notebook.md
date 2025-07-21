---
title: Jupyter Notebook
date: 2025-07-21
author: Your Name
cell_count: 39
score: 35
---

```python
#21072025
```


```python
def bubble_sort(arr):
    print("\nBubble Sort")
    n = len(arr)
    for i in range(n):
        for j in range(0, n - i - 1):
```


```python
print(f"Compare {arr[j]} and {arr[j+1]}")
```


```python
 if arr[j] > arr[j + 1]:
                print(f"Swap {arr[j]} <-> {arr[j+1]}")
```


```python
arr[j], arr[j + 1] = arr[j + 1], arr[j]
        print(f"After pass {i+1}: {arr}")  
return arr
```


```python
def insertion_sort(arr):
    print("\nInsertion Sort")
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
```


```python
 print(f"Insert {key}")
        while j >= 0 and arr[j] > key:
            print(f"Move {arr[j]} to position {j+1}")
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key
```


```python
print(f"Inserted {key}, Array now: {arr}")
    return arr
```


```python
def linear_search(arr, target):
    print(f"\nLinear Search for {target}")
    for i in range(len(arr)):
        print(f"Check index {i}: {arr[i]}")
        if arr[i] == target:
```


```python
print(f"Found {target} at index {i}")
            return i
    print("Not Found")
    return -1
```


```python
def binary_search(arr, target):
    print(f"\nBinary Search for {target}")
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high)
```


```python
print(f"Check middle index {mid}: {arr[mid]}")
        if arr[mid] == target:
            print(f"Found {target} at index {mid}")
            return mid
        elif arr[mid] < target:
```


```python
print(f"{target} > {arr[mid]} → go right")
            low = mid + 1
        else:
            print(f"{target} < {arr[mid]} → go left")
            high = mid - 1
    print("Not Found")
    return -1
```


```python
def merge_sort(arr):
    print(f"\nMerge Sort on {arr}")
    if len(arr) > 1:
        mid = len(arr) // 2
        L = arr[:mid]
        R = arr[mid:]
```


```python
print(f"Split into {L} and {R}")
        merge_sort(L)
        merge_sort(R)
        i = j = k = 0
```


```python
while i < len(L) and j < len(R):
            print(f"Compare {L[i]} and {R[j]}")
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1
```


```python
 while i < len(L):
            arr[k] = L[i]
            i += 1
            k += 1
        while j < len(R):
            arr[k] = R[j]
            j += 1
            k += 1
```


```python
print(f"Merged: {arr}")
    return arr
```


```python
def quick_sort(arr):
    print(f"\nQuick Sort on {arr}")
    if len(arr) <= 1:
        return arr
    else:
```


```python
 pivot = arr[0]
        print(f"Pivot: {pivot}")
        less = [x for x in arr[1:] if x <= pivot]
        greater = [x for x in arr[1:] if x > pivot]
        print(f"Less: {less}, Greater: {greater}")
        return quick_sort(less) + [pivot] + quick_sort(greate)
```


```python
def test_all_algorithms():
    test_array = [34, 12, 5, 66, 21]
    print("\nRunning All Algorithms on:", test_array)

    print("\n-- Bubble Sort --")
    bubble_sort(test_array.copy())
```


```python
 print("\n-- Insertion Sort --")
    insertion_sort(test_array.copy())
```


```python
print("\n-- Merge Sort --")
    merge_sort(test_array.copy())
```


```python
 print("\n-- Quick Sort --")
    sorted_qs = quick_sort(test_array.copy())
    print("Quick Sort Result:", sorted_qs)
```


```python
print("\n-- Binary Search (sorted array) --")
    sorted_arr = sorted(test_array)
    binary_search(sorted_arr, 21)
```


```python
 print("\n-- Linear Search --")
    linear_search(test_array, 66)
```


```python
def menu():
    while True:
        print("\nDSA Menu")
        print("1. Bubble Sort")
        print("2. Insertion Sort")
        print("3. Merge Sort")
        print("4. Quick Sort")
        print("5. Linear Search")
        print("6. Binary Search (sorted only)")
        print("7. Test All")
        print("8. Exit")
```


```python
 choice = input("Choose an option: ")
        arr = [29, 10, 14, 37, 14]
```


```python
if choice == '1':
            print("Original:", arr)
            bubble_sort(arr.copy())
```


```python
 elif choice == '2':
            print("Original:", arr)
            insertion_sort(arr.copy())
```


```python
elif choice == '3':
            print("Original:", arr)
            merge_sort(arr.copy())
```


```python
 elif choice == '4':
            print("Original:", arr)
            result = quick_sort(arr.copy())
            print("Sorted:", result)
```


```python
elif choice == '5':
            val = int(input("Enter value to search: "))
            linear_search(arr, val)
```


```python
elif choice == '6':
            sorted_arr = sorted(arr)
            val = int(input("Enter value to search: "))
            binary_search(sorted_arr, val)
```


```python
 elif choice == '7':
            test_all_algorithms()
        elif choice == '8':
            print("Goodbye!")
```


```python
 break
        else:
            print("Invalid choice, try again.")
```


```python
if __name__ == "__main__":
    menu()
```


```python

```


```python

```


---
**Score: 35**