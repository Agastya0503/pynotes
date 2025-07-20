---
title: Testing
date: 2025-07-21
author: Your Name
cell_count: 8
score: 5
---

```python
#20072025
```

    1 plus 2 equals 3
    3 plus 4 equals 7
    4 plus 5 equals 9
    


```python
number_pairs = [(1, 2), (3, 4), (4, 5), (10, 20), (7, 13), (15, 2
```

    enter a number:  3
    

    factorial: 6
    


```python
number = int(input("enter a number"))
for i in range(1,11):
    answer = number * i
    print(f"{number} x {i} = {answer}")
```

    enter a number 5
    

    5 x 1 = 5
    5 x 2 = 10
    5 x 3 = 15
    5 x 4 = 20
    5 x 5 = 25
    5 x 6 = 30
    5 x 7 = 35
    5 x 8 = 40
    5 x 9 = 45
    5 x 10 = 50
    


```python
numbers = [10,20,30,40]
total = 0
for i in numbers:
    total = total + i
    print("sum:", total)
```

    sum: 10
    sum: 30
    sum: 60
    sum: 100
    


```python
text = "Aku"
vowels = "aeiouAEIOU"
count = 0

for char in text:
    if char in vowels:
        count += 1

print(f"Number of vowels: {count}")
```

    Number of vowels: 2
    


```python
email = input("enter your email:")

if "@" in email and "." in email and email.index('@') < email.rindex('.'):
    print("Valid email format")
else:
    print("Invalid email format")
```

    enter your email: aku05.com
    

    Invalid email format
    


```python
num = int(input("enter a numbre"))
if num%3 == 0 and num%5 == 0:
    print("number is divisible by 3 and 5")
else:
    print("number is not divisible by 3 and 5")
```

    enter a numbre 5
    

    number is not divisible by 3 and 5
    


```python

```


---
**Score: 5**