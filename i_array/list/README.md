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
fruits = ['Apple', 'Banana', 'Blackberry', 'Orange', 'Strawberry']

# List comprehension
numbers = [i for i in range(9+1)]  # numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

### Traversal

```python
fruits = ['Apple', 'Banana', 'Blackberry', 'Orange', 'Strawberry']

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
fruits = ['Apple', 'Banana', 'Blackberry', 'Orange', 'Strawberry']

# Via index
element = fruits[2]

# Slicing
# Syntax: the_list[start_index:end_index] or the_list[start_index:end_index:step_size]
print(fruits[1:2+1])  # ['Banana', 'Blackberry']
print(fruits[::2])  # ['Apple', 'Blackberry', 'Strawberry']
print(fruits[::-1])  # ['Strawberry', 'Orange', 'Blackberry', 'Banana', 'Apple']
print(fruits[::-2])  # ['Strawberry', 'Blackberry', 'Apple']
```

### Modification

#### Insertion

```python
fruits = ['Apple', 'Banana', 'Strawberry']

# At the beginning
fruits.insert(0, 'Blackberry')  # fruits = ['Blackberry', 'Apple', 'Banana', 'Strawberry']

# At the end of the list
fruits.append('Cherry')  # fruits = ['Blackberry', 'Apple', 'Banana', 'Strawberry', 'Cherry']

# At any index using insert()
fruits.insert(2, 'Blackberry')  # fruits = ['Blackberry', 'Apple', 'Blackberry', 'Banana', 'Strawberry', 'Cherry']

# At any index using slicing
index, element = 3, 'Kiwi'
fruits = fruits[:index] + [element] + fruits[index:]
print(fruits)  # ['Blackberry', 'Apple', 'Blackberry', 'Kiwi', 'Banana', 'Strawberry', 'Cherry']
```

#### Deletion

```python
fruits = ['Blackberry', 'Apple', 'Blackberry', 'Banana', 'Strawberry', 'Cherry', 'Kiwi', 'Grape']

# Delete and return the last element
element = fruits.pop()  # fruits = ['Blackberry', 'Apple', 'Blackberry', 'Banana', 'Strawberry', 'Cherry', 'Kiwi']

# Delete and return the ith element
ith_element = fruits.pop(2)  # fruits = ['Blackberry', 'Apple', 'Banana', 'Strawberry', 'Cherry', 'Kiwi']

# Delete the last element using slicing
fruits = fruits[:-1]  # fruits = ['Blackberry', 'Apple', 'Banana', 'Strawberry', 'Cherry']

# Delete the last element using del
del fruits[-1]  # ['Blackberry', 'Apple', 'Banana', 'Strawberry']

# Delete item at an index using del
del fruits[2]  # ['Blackberry', 'Apple', 'Strawberry']

# Delete item at an index using slicing
index = 1
fruits = fruits[:index] + fruits[index+1:]  # ['Blackberry', 'Strawberry']

# Clear the list
fruits.clear()  # fruits = []

fruits = ['Blackberry', 'Apple', 'Blackberry', 'Banana', 'Banana', 'Kiwi']

# Remove the first occurrence of an element
fruits.remove('Blackberry')  # fruits = ['Apple', 'Blackberry', 'Banana', 'Banana', 'Kiwi']

# Remove all occurrence of an element using remove()
item = 'Banana'
while item in fruits:
  fruits.remove(item)
print(fruits)  # ['Apple', 'Blackberry', 'Kiwi']
```

### Extension

```python
numbers = [1, 2]
numbers.extend([3, 4])  # numbers = [1, 2, 3, 4]
numbers += [5, 6]  # numbers = [1, 2, 3, 4, 5, 6]
```

### Manipulation

#### Reversal

```python
fruits = ['Apple', 'Orange', 'Strawberry', 'Banana', 'Blackberry']

# Reverse using slicing
fruits_reversed = fruits[::-1]

# In-place reverse using reverse()
fruits.reverse()

# Reverse using reversed() - returns a reverse iterator object
numbers = reversed([1, 2, 3, 4, 5, 6])  # numbers = <list_reverseiterator object at 0x1092e0dc0>
for number in numbers:
  print(number)
```

#### Sorting

```python
fruits = ['Apple', 'Orange', 'Strawberry', 'Banana', 'Blackberry']

# Sorting out-of-place with sorted() in ascending order
fruits_sorted = sorted(fruits)  # fruits_sorted = ['Apple', 'Banana', 'Blackberry', 'Orange', 'Strawberry']

# Sorting out-of-place with sorted() in descending order
data = sorted(fruits, reverse=True)  # data = ['Strawberry', 'Orange', 'Blackberry', 'Banana', 'Apple']

# Sorting in-place with sort() in ascending order
fruits.sort()  # fruits = ['Apple', 'Banana', 'Blackberry', 'Orange', 'Strawberry']

# Sorting in-place with sort() in descending order
fruits.sort(reverse=True)  # fruits = ['Strawberry', 'Orange', 'Blackberry', 'Banana', 'Apple']
```

#### Copy

TODO

#### Discovery

```python
fruits = ['Apple', 'Banana', 'Orange', 'Strawberry', 'Banana', 'Blackberry']

# Get the index value of first occurrence
print(fruits.index('Banana'))  # 1

# Get the count of the element
print(fruits.count('Banana'))  # 2
```

#### Concatenation and Repetition

```python

# Concatenation
left = [1, 2, 3]
right = [4, 5, 6]
numbers = left + right  # numbers = [1, 2, 3, 4, 5, 6]

# Repetition
print([1, 2] * 3)  # [1, 2, 1, 2, 1, 2]
```
