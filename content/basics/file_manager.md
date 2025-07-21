---
title: File Manager
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

def list_files(directory: str):
    print(f"\n Listing all files in: {directory}")
```


```python
 try:
        files = os.listdir(directory)
        if not files:
```


```python
print(" No files found.")
```


```python
return []
        print("Files:")
```


```python
 for idx, file in enumerate(files):
            print(f"{idx + 1}. {file}")
```


```python
 return files
    except FileNotFoundError:
```


```python
 print("Error: The specified directory does not exist.")
        return []
```


```python
def read_file(filepath: str):
    print(f"\nReading file: {filepath}")
```


```python
 try:
        with open(filepath, 'r', encoding='utf-8') as f:
            content = f.read()
```


```python
print("File opened successfully.")
            print("\n--- Start of File ---")
            print(content[:500])  # Print first 500 characters
            print("--- End of Preview ---")
```


```python
return content
    except FileNotFoundError:
```


```python
print("Error: File not found.")
```


```python
return ""
    except UnicodeDecodeError:
```


```python
print("Error: File is not a readable text file.")
return ""
```


```python
def file_statistics(filepath: str):
    print(f"\nGetting statistics for: {filepath}")
```


```python
content = read_file(filepath)
    if not content:
```


```python
  print("No content to analyze.")
        return
```


```python
 words = content.split()
    lines = content.splitlines()
```


```python
print(f"Total lines: {len(lines)}")
    print(f"Total words: {len(words)}")
    print(f"Total characters: {len(content)}")
```


```python
def search_word(filepath: str, word: str):
    print(f"\nSearching for '{word}' in {filepath}")
```


```python
content = read_file(filepath)
    if not content:
```


```python
 print("No content available to search.")
        return
```


```python
lines = content.splitlines()
    found = False
```


```python
for i, line in enumerate(lines):
        if word in line:
```


```python
 print(f"Found in line {i + 1}: {line.strip()}")
            found = True
```


```python
if not found:
        print(f"The word '{word}' was not found in the file.")
```


```python
def file_manager_menu():
    while True:
```


```python
print("\n=== File Manager CLI ===")
        print("1. List files in a directory")
        print("2. Read a file")
        print("3. Show file statistics")
        print("4. Search for a word in a file")
        print("0. Exit")
```


```python
choice = input("Enter your choice: ")
```


```python
if choice == '1':
            dir_path = input("Enter directory path: ")
            list_files(dir_path)
```


```python
elif choice == '2':
            file_path = input("Enter full file path: ")
            read_file(file_path)
```


```python
elif choice == '3':
            file_path = input("Enter full file path: ")
            file_statistics(file_path)
```


```python
elif choice == '4':
            file_path = input("Enter full file path: ")
            word = input("Enter the word to search for: ")
            search_word(file_path, word)
```


```python
elif choice == '0':
            print("Exiting File Manager.")
```


```python
 break
```


```python
 else:
            print("Invalid option. Please try again.")
```


```python
if __name__ == "__main__":
    file_manager_menu()
```


---
**Score: 35**