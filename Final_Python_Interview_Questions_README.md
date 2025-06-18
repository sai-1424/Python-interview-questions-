
# Python Interview Questions
### Prepared by Leela

---

## 1. Difference between List and Tuple in Python?

Lists are mutable, meaning their content can be changed after creation, while tuples are immutable.  
Lists use square brackets `[]`, and tuples use parentheses `()`.  
Lists are slower than tuples but more flexible for dynamic data.

```python
my_list = [1, 2, 3]
my_tuple = (1, 2, 3)
```

---

## 2. How do sets help in removing duplicates from a list?

Sets store only unique elements, automatically removing duplicates.  
Converting a list to a set filters out repeated values.  
This is useful for data cleanup tasks.

```python
data = ["Leela", "Leela", "Asha"]
unique = list(set(data))
print(unique)  # ['Asha', 'Leela']
```

---

## 3. Why are dictionaries faster than lists for lookups?

Dictionaries use hash tables to find keys in constant time.  
Lists require checking each item, which is slower.  
For quick data access, dictionaries are ideal.

```python
d = {"Leela": 22, "Asha": 20}
print(d["Leela"])  # 22
```

---

## 4. How are Python strings immutable if they allow operations like replace()?

Strings cannot be changed once created; methods like `replace()` return a new string.  
Original strings remain unchanged, preserving immutability.  
This behavior avoids unexpected side-effects.

```python
name = "Leela"
print(name.replace("L", "M"))  # 'Meela'
print(name)  # 'Leela'
```

---

## 5. How do you merge two dictionaries in Python latest version?

Python 3.9+ allows merging with the `|` operator.  
This combines key-value pairs from both dictionaries.  
If keys overlap, the second dictionary's values are used.

```python
d1 = {"Leela": 22}
d2 = {"Asha": 23}
merged = d1 | d2
print(merged)  # {'Leela': 22, 'Asha': 23}
```

---

## 6. Explain dictionary comprehension with example?

It creates dictionaries using a single line from iterable data.  
Format: `{key: value for item in iterable}`.  
Useful for generating mappings like squares or uppercase names.

```python
squares = {x: x**2 for x in range(3)}
print(squares)  # {0: 0, 1: 1, 2: 4}
```

---

## 7. What are nested dictionaries and how do you access inner values?

Nested dictionaries have dictionaries inside other dictionaries.  
Inner values are accessed using chained keys.  
They're useful for structured data like student records.

```python
student = {"Leela": {"age": 22, "grade": "A"}}
print(student["Leela"]["grade"])  # 'A'
```

---

## 8. How can you convert a list of tuples into a dictionary?

Use the `dict()` function to convert a list of tuples.  
Each tuple must have two elements (key, value).  
This is handy when data is already structured as pairs.

```python
pairs = [("Leela", 22), ("Asha", 20)]
d = dict(pairs)
print(d)  # {'Leela': 22, 'Asha': 20}
```

---

## 9. How would you handle a missing key in a dictionary?

Use `get()` to provide a default if the key is missing.  
This prevents KeyError and makes code safer.  
Also consider `defaultdict` for complex cases.

```python
d = {"Leela": 22}
print(d.get("Asha", "Not Found"))  # 'Not Found'
```

---

## 10. Can we use a list as a key in a dictionary? Why or why not?

No, lists are mutable and unhashable.  
Dictionary keys must be immutable and hashable.  
Use tuples instead if the key needs multiple values.

```python
# d = {[1, 2]: "Leela"}  # ❌ Invalid
d = {(1, 2): "Leela"}    # ✅ Valid
```

---

## 11. What happens if you try to add a mutable object to a set?

Sets require elements to be hashable (immutable).  
Trying to add a list or dict raises `TypeError`.  
Use tuples or strings instead.

```python
s = set()
# s.add([1, 2])  # ❌ Raises TypeError
s.add((1, 2))    # ✅ Valid
```

---

## 12. Write code to find common elements in two lists using set operations?

Convert both lists to sets and use intersection.  
This finds shared elements quickly.  
It’s efficient and readable.

```python
a = ["Leela", "Asha", "Ravi"]
b = ["Asha", "Ravi", "Kiran"]
common = list(set(a) & set(b))
print(common)  # ['Asha', 'Ravi']
```

---

## 13. What is the difference between `is` and `==` for strings? What is the syntax?

`==` checks value equality; `is` checks identity (memory address).  
Use `==` for comparison and `is` for identity testing.  
They may return same result for strings due to caching.

```python
name1 = "Leela"
name2 = "Leela"
print(name1 == name2)  # True
print(name1 is name2)  # True (in CPython)
```

---

## 14. How does slicing work in tuple and string? What is the syntax?

Slicing uses `[start:stop:step]` to extract parts of a sequence.  
Works with strings, lists, and tuples.  
Negative indices count from the end.

```python
name = "Leela"
print(name[1:4])  # 'eel'
t = (10, 20, 30, 40)
print(t[:2])      # (10, 20)
```

---

## 15. How can you reverse a string or list in Python using slicing?

Use `[::-1]` to reverse a sequence using slicing.  
This works with lists, strings, and tuples.  
It’s a simple and fast technique.

```python
name = "Leela"
print(name[::-1])  # 'aleeL'
nums = [1, 2, 3]
print(nums[::-1])  # [3, 2, 1]
```

---

✅ **Prepared with 💻 by Leela**
