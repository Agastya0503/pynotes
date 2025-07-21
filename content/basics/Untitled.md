---
title: Untitled
date: 2025-07-21
author: Your Name
cell_count: 32
score: 30
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

```


```python

```


```python

```


```python

```


---
**Score: 30**