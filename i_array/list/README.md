# List in Python

> Author: Himel Das

List is a data structure used to store a collection of items. List is ordered, indexed, mutable, heterogeneous, and
dynamic.

Characteristics of list:

- Ordered: List contains the order of added items.
- Indexed: List elements can be accessed via their index. If `n` is the length of the list, `0` is the lower limit and
  `n-1` is the upper limit of the list index.
- Mutable: After the creation of the list, elements can be added, changed, or deleted.
- Heterogeneous: A list can contain stores items of various data types.
- Dynamic: A list can dynamically resize to accommodate new items.

Example: `data = [200, None, True, 'sky', 19.223]`

## Methods and Operations that can be Performed with List

### Creation

```python
# Empty list
cities = []
countries = list()

# List with elements
fruits = ["Apple", "Banana", "Blackberry", "Orange", "Strawberry"]

# List comprehension
numbers = [i for i in range(9+1)]  # numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

### Traversal

```python
fruits = ["Apple", "Banana", "Blackberry", "Orange", "Strawberry"]

for fruit in fruits:
    print(fruit)

for i in range(len(fruits)):
    print(fruits[i])

i = 0
while i < len(fruits):
    print(fruits[i])
    i += 1
```

### Access

```python
fruits = ["Apple", "Banana", "Blackberry", "Orange", "Strawberry"]

# Via index
element = fruits[2]

# Slicing
# Syntax: the_list[start_index:end_index] or the_list[start_index:end_index:step_size]
print(fruits[1:2+1])  # ['Banana', 'Blackberry']
print(fruits[::2])  # ['Apple', 'Blackberry', 'Strawberry']
print(fruits[::-1])  # ['Strawberry', 'Orange', 'Blackberry', 'Banana', 'Apple']
print(fruits[::-2])  # ['Strawberry', 'Blackberry', 'Apple']
```
