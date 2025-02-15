# Sets in Python
It will describe about operations on sets in python
Sets are a fundamental data type in Python used to store collections of unique elements. They are unordered, meaning the elements are not stored in any particular order, and they do not allow duplicate values. Sets are useful for tasks like membership testing, removing duplicates, and performing mathematical set operations like union, intersection, and difference.

---

**Here are the basics of working with sets in Python:**

## Creating a Set
  
  You can create a set by enclosing elements in curly braces {} or by using the set() function.
  
  
### Using curly braces


```
my_set = {1, 2, 3, 4, 5}
print(my_set)  # Output: {1, 2, 3, 4, 5}
```

### Using the set() function

```
another_set = set([1, 2, 3, 4, 5])  # Pass a list or iterable
print(another_set)  # Output: {1, 2, 3, 4, 5}

# Empty set (use set(), not {})
empty_set = set()
print(empty_set)  # Output: set()
```

---

## Properties of Sets

    1. Unordered: Elements are not stored in any specific order.

    2. Unique Elements: Duplicates are automatically removed.

    3.  Mutable: You can add or remove elements, but the elements themselves must be immutable (e.g., numbers, strings, tuples).

** Duplicates are removed**
```
my_set = {1, 2, 2, 3, 3, 3}
print(my_set)  # Output: {1, 2, 3}
```
## Adding and Removing Elements

  Use add() to add a single element.

  Use update() to add multiple elements.

  Use remove() or discard() to remove an element. remove() raises an error if the element doesn't exist, while discard()     does not.
```
my_set = {1, 2, 3}

# Add an element
my_set.add(4)
print(my_set)  # Output: {1, 2, 3, 4}

# Add multiple elements
my_set.update([5, 6, 7])
print(my_set)  # Output: {1, 2, 3, 4, 5, 6, 7}

#Remove an element
my_set.remove(3)
print(my_set)  # Output: {1, 2, 4, 5, 6, 7}

#Discard an element (no error if element doesn't exist)
my_set.discard(10)
print(my_set)  # Output: {1, 2, 4, 5, 6, 7}
```
## Set Operations
Sets support mathematical operations like union, intersection, difference, and symmetric difference.
```
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# Union (elements in either set)

print(set1 | set2)  # Output: {1, 2, 3, 4, 5, 6}

# Intersection (elements in both sets)
print(set1 & set2)  # Output: {3, 4}

# Difference (elements in set1 but not in set2)
print(set1 - set2)  # Output: {1, 2}

#Symmetric Difference (elements in either set but not in both)

print(set1 ^ set2)  # Output: {1, 2, 5, 6}
```
## Checking Membership
You can check if an element exists in a set using the in keyword.
```
my_set = {1, 2, 3, 4, 5}
print(3 in my_set)  # Output: True
print(10 in my_set)  # Output: False
```
## Set Methods

**Here are some commonly used set methods:**

### Method	Description:
```
  add()	Adds an element to the set.
  update()	Adds multiple elements to the set.
  remove()	Removes an element (raises error if not found).
  discard()	Removes an element (no error if not found).
  pop()	Removes and returns an arbitrary element.
  clear()	Removes all elements from the set.
  union()	Returns the union of two sets.
  intersection()	Returns the intersection of two sets.
  difference()	Returns the difference of two sets.
  symmetric_difference()	Returns the symmetric difference of two sets.
```
## Frozen Sets
A frozen set is an immutable version of a set. Once created, you cannot modify it.
```
frozen_set = frozenset([1, 2, 3, 4])
print(frozen_set)  # Output: frozenset({1, 2, 3, 4})

# Frozen sets are immutable
# frozen_set.add(5)  # This will raise an error
```
## Practical Use Cases

Removing duplicates: Convert a list to a set to remove duplicates.

Membership testing: Sets are optimized for checking if an element exists.

Mathematical operations: Perform union, intersection, etc., on collections.
```
# Remove duplicates from a list
my_list = [1, 2, 2, 3, 3, 3]
unique_elements = set(my_list)
print(unique_elements)  # Output: {1, 2, 3}
```

