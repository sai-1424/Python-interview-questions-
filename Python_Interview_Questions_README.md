
# Python Interview Questions
### Prepared by Leela

---

## 1. Difference between List and Tuple in Python?

The primary difference between lists and tuples in Python is their mutability:
Lists are mutable: This means that after a list is created, its elements can be modified, added, or removed. Lists are defined using square brackets [].
Python
    my_list = [1, 2, 3]
    my_list.append(4)  # Modifying the list
    print(my_list)  # Output: [1, 2, 3, 4]
    
Tuples are immutable: This means that once a tuple is created, its elements cannot be changed, added, or removed. Tuples are defined using parentheses ().
Python
example:
    my_tuple = (1, 2, 3)
    # my_tuple.append(4)  # This would raise an AttributeError
    print(my_tuple)  # Output: (1, 2, 3)

---

## 2. How do sets help in removing duplicates from a list?

Sets are unordered collections that store only unique items. When a list is converted into a set, all duplicates are automatically removed.

```python
a = [1, 2, 2, 3]
unique = list(set(a))
print(unique)  # Output: [1, 2, 3]
```

---

## 3. Why are dictionaries faster than lists for lookups?

Dictionaries use hash tables to store key-value pairs, allowing constant time lookup, while lists require linear search.

```python
d = {'a': 1, 'b': 2}
print(d['a'])  # Fast lookup using key
```

---

## 4. How are Python strings immutable if they allow operations like replace()?

String operations like `replace()` return a new string rather than modifying the original. This maintains immutability.

```python
s = "hello"
print(s.replace("h", "y"))  # Output: 'yello'
print(s)                    # Original: 'hello'
```

---

## 5. How do you merge two dictionaries in Python latest version?

In Python 3.9+, the `|` operator merges dictionaries. If keys overlap, the right-side dictionary's value takes precedence.

```python
dict1 = {'a': 1}
dict2 = {'b': 2}
merged = dict1 | dict2
print(merged)  # {'a': 1, 'b': 2}
```

---

## 6. Explain dictionary comprehension with example?

It is a concise way to create dictionaries from iterables using a single line of code.

```python
squares = {x: x**2 for x in range(5)}
print(squares)  # {0:0, 1:1, 2:4, 3:9, 4:16}
```

---

## 7. What are nested dictionaries and how do you access inner values?

Nested dictionaries are dictionaries inside other dictionaries. You access inner values using chained keys.

```python
data = {'person': {'name': 'Leela', 'age': 22}}
print(data['person']['name'])  # Output: Leela
```

---

## 8. How can you convert a list of tuples into a dictionary?

The `dict()` constructor can convert a list of key-value tuples to a dictionary.

```python
tuples = [('a', 1), ('b', 2)]
d = dict(tuples)
print(d)  # {'a': 1, 'b': 2}
```

---

## 9. How would you handle a missing key in a dictionary?

Use `get()` or `defaultdict` to avoid errors when keys are missing.

```python
d = {'a': 1}
print(d.get('b', 'Not Found'))  # Output: Not Found
```

---

## 10. Can we use a list as a key in a dictionary? Why or why not?

No, because lists are mutable and unhashable, and dictionary keys must be immutable.

```python
# This will raise TypeError
# d = {[1, 2]: "value"} 
```

---

## 11. What happens if you try to add a mutable object to a set?

Mutable objects like lists are unhashable and can't be added to a set.

```python
# set().add([1, 2])  # Raises TypeError
```

---

## 12. Write a code to find common elements in two lists using set operations?

Use set intersection (`&`) to find common items.

```python
a = [1, 2, 3]
b = [2, 3, 4]
common = list(set(a) & set(b))
print(common)  # [2, 3]
```

---

## 13. What is the difference between `is` and `==` for strings?

`==` checks value equality, `is` checks memory address (identity).

```python
a = "hello"
b = "hello"
print(a == b)  # True
print(a is b)  # True (sometimes due to string interning)
```

---

## 14. How does slicing work in tuple and string?

Slicing extracts parts of sequences using `[start:stop:step]` syntax.

```python
s = "python"
t = (10, 20, 30)
print(s[1:4])  # 'yth'
print(t[:2])   # (10, 20)
```

---

## 15. How can you reverse a string or list in Python using slicing?

Use `[::-1]` to reverse sequences.

```python
s = "leela"
print(s[::-1])  # 'aleel'

l = [1, 2, 3]
print(l[::-1])  # [3, 2, 1]
```

---

✅ **Prepared with 💻 by Leela**
