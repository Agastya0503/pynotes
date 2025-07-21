---
title: Insertion Sort
date: 2025-07-21
author: Your Name
cell_count: 38
score: 35
---

```python
#21072025
```


```python
import os
TASKS_FILE = "tasks.txt"
```


```python
def load_tasks():
    print("Loading tasks from file...")
```


```python
tasks = []
    if os.path.exists(TASKS_FILE):
        with open(TASKS_FILE, 'r') as f:
            lines = f.readlines()
            for line in lines:
```


```python
status, task = line.strip().split("||")
                tasks.append({"task": task, "done": status == "1"})
```


```python
print(f"Loaded {len(tasks)} tasks.")
```


```python
 else:
        print("No existing task file found. Starting with an empty task list.")
    return tasks
```


```python
def save_tasks(tasks):
    print("Saving tasks to file...")
```


```python
 with open(TASKS_FILE, 'w') as f:
        for t in tasks:
            line = f"{'1' if t['done'] else '0'}||{t['task']}\n"
            f.write(line)
```


```python
 print("Tasks saved successfully.")
```


```python
def add_task(tasks):
    task = input("Enter a new task: ").strip()
```


```python
if task:
        tasks.append({"task": task, "done": False})
```


```python
 print(f"Task added: {task}")
```


```python
  else:
        print("Empty task not added.")
```


```python
def view_tasks(tasks):
    if not tasks:
```


```python
print("No tasks to show.")
        return
```


```python
print("\nYour Task List:")
```


```python
for idx, t in enumerate(tasks):
        status = "✓ Done" if t["done"] else "⨯ Pending
```


```python
print(f"{idx + 1}. {t['task']} - {status}")
    print(f"Total: {len(tasks)} task(s)")
```


```python
def mark_complete(tasks):
    view_tasks(tasks)
    if not tasks:
        return
    try:
```


```python
index = int(input("Enter task number to mark complete: ")) - 1
        if 0 <= index < len(tasks):
            tasks[index]["done"] = True
```


```python
 print(f"Marked task '{tasks[index]['task']}' as complete.")
```


```python
 else:
            print("Invalid task number.")
```


```python
except ValueError:
        print("Invalid input. Please enter a number.")
```


```python
def delete_task(tasks):
    view_tasks(tasks)
    if not tasks:
        return
```


```python
 try:
        index = int(input("Enter task number to delete: ")) - 1
        if 0 <= index < len(tasks):
            deleted = tasks.pop(index)
```


```python
print(f"Deleted task: {deleted['task']}")
```


```python
else:
            print("Invalid task number.")
```


```python
 except ValueError:
        print("Invalid input. Please enter a number.")
```


```python
def main_menu():
    tasks = load_tasks()
    while True:
```


```python
 print("\n=== Task Manager Menu ===")
        print("1. Add Task")
        print("2. View Tasks")
        print("3. Mark Task as Complete")
        print("4. Delete Task")
        print("5. Save & Exit")
```


```python
 choice = input("Choose an option (1-5): ").strip()
```


```python
if choice == '1':
            add_task(tasks)
        elif choice == '2':
            view_tasks(tasks)
        elif choice == '3':
            mark_complete(tasks)
```


```python
elif choice == '4':
            delete_task(tasks)
        elif choice == '5':
            save_tasks(tasks)
            print("Goodbye. Tasks saved.")
            break
```


```python
 else:
            print("Invalid choice. Please try again.")
```


```python
if __name__ == "__main__":
    main_menu()
```


```python

```


```python

```


---
**Score: 35**