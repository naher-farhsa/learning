# 🚀 Python Interview Prep Planner (Java → Python Mode)

---

# 📅 Overview
- Duration: **2 Weeks (Fast-Track)**
- Goal: **Crack Python interviews using Java mental model translation**
- Focus: **Traps + Output + Coding (NOT theory overload)**

---

# 📘 THEORY (IN-DEPTH REVISION — MUST DO)

## 🟢 Core Python (High Priority)

| Topic | What They Ask | Java vs Python Insight | Duration | Resources |
|------|--------------|----------------------|----------|----------|
| Data Types | mutable vs immutable | String immutable (Java) vs list mutable | 1 hr | https://realpython.com/python-data-types/ |
| Lists vs Tuples | when to use | Tuple = like final array | 45 min | https://www.geeksforgeeks.org/python-tuples-vs-lists/ |
| Dict & Set | hashing, collisions | Like HashMap but cleaner syntax | 1 hr | https://realpython.com/python-dicts/ |
| Functions | default args trap | ⚠️ mutable default bug | 1 hr | https://docs.python.org/3/tutorial/controlflow.html |
| *args, **kwargs | variable args | Like varargs + map | 45 min | https://realpython.com/python-kwargs-and-args/ |
| Pass by Object Ref | behavior | Hybrid of value + reference | 1 hr | https://realpython.com/python-pass-by-reference/ |
| List Comprehension | syntax sugar | Java Streams lite | 1 hr | https://realpython.com/list-comprehension-python/ |

---

## 🟡 Intermediate (Must for Interviews)

| Topic | What They Ask | Key Insight | Duration | Resources |
|------|--------------|------------|----------|----------|
| Decorators | how they work | Function wrapping | 1.5 hr | https://realpython.com/primer-on-python-decorators/ |
| Generators | yield vs return | Lazy evaluation | 1 hr | https://realpython.com/introduction-to-python-generators/ |
| Iterators | iter / next | Internal working | 1 hr | https://www.programiz.com/python-programming/iterator |
| Lambda | use cases | small inline functions | 30 min | https://realpython.com/python-lambda/ |
| Exception Handling | custom exceptions | Cleaner than Java | 45 min | https://docs.python.org/3/tutorial/errors.html |
| Modules & Imports | import system | Python path magic | 45 min | https://realpython.com/python-modules-packages/ |

---

## 🔴 Advanced (High Signal Questions)

| Topic | What They Ask | Why Important | Duration | Resources |
|------|--------------|--------------|----------|----------|
| GIL | threading limitation | ⭐ Very common | 1 hr | https://realpython.com/python-gil/ |
| Multithreading vs Multiprocessing | use cases | CPU vs IO bound | 1 hr | https://realpython.com/python-concurrency/ |
| Memory Management | ref count, GC | hidden behavior | 1 hr | https://www.geeksforgeeks.org/garbage-collection-python/ |
| Deep vs Shallow Copy | copy pitfalls | mutable bug source | 45 min | https://realpython.com/python-copy/ |
| OOP in Python | dunder methods | Python-style OOP | 1 hr | https://realpython.com/python3-object-oriented-programming/ |
| Context Managers | with keyword | resource handling | 45 min | https://realpython.com/python-with-statement/ |

---

# 💻 PRACTICAL (CODING + OUTPUT TRAPS)

## 🔥 Output-Based Questions (MOST IMPORTANT)

### Mutable Default Argument
```python
def add_item(item, lst=set()):
    lst.add(item)
    return lst

print(add_item(1))
print(add_item(2))
```
👉 Shared state across calls

---

### Closure Trap
```python
funcs = []
for i in range(3):
    funcs.append(lambda: i)

print([f() for f in funcs])
```
👉 Output: [2,2,2]

---

### List Reference Trap
```python
a = [[1,2]] * 3
a[0][0] = 99
print(a)
```
👉 Output: all modified

---

### is vs ==
```python
a=[1,2]
b=[1,2]
print(a==b, a is b)
```
👉 Output: True False

---

### Generator Exhaustion
```python
def gen():
 yield 1
 yield 2

g=gen()
print(list(g))
print(list(g))
```
👉 Output: second empty

---

## 🧠 Coding Questions

### Easy
- Two Sum
- Reverse String
- Palindrome
- Frequency Counter

### Medium
- Group Anagrams
- Top K Frequent Elements
- Merge Intervals
- LRU Cache

### Python-Specific
- Implement Decorator
- Custom Iterator
- Generator-based Fibonacci
- Context Manager

---

# 🗓️ WEEKLY + DAILY EXECUTION PLAN

## WEEK 1 — Core + Concepts
- Day 1: Data Types + Collections
- Day 2: Functions + Args
- Day 3: Pythonic Code
- Day 4: Iterators + Generators
- Day 5: Decorators + Context Manager
- Day 6: GIL + Concurrency
- Day 7: Revision + Output Start

## WEEK 2 — Coding + Interview Mode
- Day 8: Output Practice (Core)
- Day 9: Output Practice (Advanced)
- Day 10: Easy Coding
- Day 11: Medium Coding
- Day 12: Python-Specific Coding
- Day 13: Mock Interview
- Day 14: Final Revision

---

# 🔄 JAVA → PYTHON MAP

| Java | Python |
|------|--------|
| ArrayList | list |
| HashMap | dict |
| final | tuple |
| Streams | list comprehension |
| Interfaces | duck typing |

---

# 🎯 STRATEGY
- 60% → output
- 30% → coding
- 10% → theory

👉 Focus on traps = success

