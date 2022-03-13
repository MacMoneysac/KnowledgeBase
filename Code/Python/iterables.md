# Iterables


## Definition

Container: Familiar examples of iterables include **lists, tuples, and strings** - any such sequence can be iterated over in a for-loop. We will also encounter important non-sequential collections, like dictionaries and sets; these are iterables as well. It is also possible to have an iterable that “generates” each one of its members upon iteration - meaning that it doesn’t ever store all of its members in memory at once.

## Lists

List are **variable**, you can add and remove (different types of) objects on the fly. (Arrays are unmutable)

```python
sequence = [ 1, 2, 3 ]
items = [ ("Product1", 10), ("Product2", 9), ("Product3", 12) ]
```

## Tuples

A tuple is a collection which is ordered and unchangeable 

```python
point = (1, 2)

print(point[1])
```
Once a tuple is created, you cannot add items to it


## Sets

A set is a collection which is **unordered** and **unindexed**.
```python
numbers = {1, 2, 3, 4}
numbers = set(list of numbers)

if x in numbers:
    print(x)
```
Once a set is created, you cannot change its items, but you can add new items.



## Dictionaries

Collection of Key-Value pairs, Use also {} like **set**, but needs keywords, It can't be sorted

```python
point = {"x": 1, "y": 1337} 
point = dict(x=1, y=2)

if "x" in point:
    print(point["x"])
    
# Add new item
point["z"] = 42
    
print(point.get("a", 0))
# With 0 as default

another_dictionary = {**point}

for key, value in point.items():
    print(key, value)

del point["x"]
```


## Arrays

only to handle list with 10.000 Objects; more performance
"Dont solve problems that doesn't exist"
Only one type of datastructure

```python
from array import array

numbers = array("__datastructure__", [1, 2, 3, ...])
```

## Unpacking

```python
* for only Key, 
** for key-value pairs

```

## Sorting

```python
print(sorted(any_iterable))
```
Note: sorted(...) returns a list, but i doesn affect the iterable inside the function


