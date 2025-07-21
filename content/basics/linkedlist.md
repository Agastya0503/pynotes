---
title: Linkedlist
date: 2025-07-21
author: Your Name
cell_count: 25
score: 25
---

```python
#21072025
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
def insert_at_beginning(self, data):
        print(f"Inserting {data} at the beginning")
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node
        self.display()
```


```python
 def insert_at_end(self, data):
        print(f"Inserting {data} at the end")
        new_node = Node(data)
        if self.head is None:
            self.head = new_node
            self.display()
            return
```


```python
current = self.head
        while current.next:
            current = current.next
        current.next = new_node
        self.display()
```


```python
def delete_node(self, key):
        print(f"Deleting node with value {key}")
        current = self.head
```


```python
if current is not None and current.data == key:
            self.head = current.next
            print(f"Deleted head node {key}")
            self.display()
            return
```


```python
prev = None
        while current is not None and current.data != key:
            prev = current
            current = current.next
```


```python
if current is None:
            print("Node not found.")
            return
```


```python
 prev.next = current.next
        print(f"Deleted node {key}")
        self.display()
```


```python
def search(self, key):
        print(f"Searching for {key} in the list")
        current = self.head
        index = 0
        while current:
```


```python
print(f"Checking node at index {index} with value {current.data}")
            if current.data == key:
                print(f"Found {key} at index {index}")
                return index
            current = current.next
```


```python
index += 1
        print(f"{key} not found in the list")
        return -1
```


```python
 def reverse(self):
        print("Reversing the linked list")
        prev = None
        current = self.head
        while current:
```


```python
next_node = current.next
            current.next = prev
            prev = current
            current = next_node
        self.head = prev
        print("Linked list reversed")
        self.display()
```


```python
def display(self):
        current = self.head
        values = []
        while current:
            values.append(str(current.data))
            current = current.next
        print("Linked List:", " -> ".join(values) if values else "Empty")
```


```python
def menu():
    ll = LinkedList()
    while True:
        print("\nLinked List Operations Menu")
        print("1. Insert at beginning")
        print("2. Insert at end")
        print("3. Delete a node")
        print("4. Search for a value")
        print("5. Reverse the list")
        print("6. Display list")
        print("7. Exit")
```


```python
 choice = input("Enter your choice: ")

        if choice == '1':
            data = int(input("Enter value to insert at beginning: "))
            ll.insert_at_beginning(data)
```


```python
elif choice == '2':
            data = int(input("Enter value to insert at end: "))
            ll.insert_at_end(data)
```


```python
elif choice == '3':
            key = int(input("Enter value to delete: "))
            ll.delete_node(key)
```


```python
 elif choice == '4':
            key = int(input("Enter value to search: "))
            ll.search(key)
```


```python
 elif choice == '5':
            ll.reverse()
        elif choice == '6':
            ll.display()
        elif choice == '7':
```


```python
 print("Exiting program.")
            break
        else:
            print("Invalid choice. Try again.")
```


```python
if __name__ == "__main__":
    menu()
```


---
**Score: 25**