# Data Structures

There are 4 different data structures. They each have their own properties and best practices.

Every single thing in Python is an object.


---
## List (list)

- `[]` square brackets
- ordered
- indexable
- mutable
- iterable

A list in Python can be casted using the keyword `list`. A list is like a basket of data, or an array.

For example, define variables that are lists:
```python
e = []
x = [1, 2, 3]
y = ["one", "two"]
ee = list()
```
Both `e` and `ee` are empty lists. This is because the word`list` is a built-in function.

The instance methods associated with a `list` object are as follows:

- **append** is used to add something new to the end of an array.
```python
>>> x = [1, 2, 3]
>>> x.append(4)
>>> x
[1, 2, 3, 4]
```

- **clear** clears a list and makes it empty.

- **copy** creates a copy with a new address.
```python
>>> x = [1, 2, 3]
>>> y = x.copy()
>>> id(x), id(y)
(139999573, 284894802)
```

- **count** counts the frequency of a specified value in a list (iterable). (E.g., how many times does the number `4` appear?)

- **extend** extends one array with another at the end. It permanently changes the array. (If you are working with a mutable data type, assume it's changing.)
```python
>>> x = [1, 2, 3]
>>> y = [4, 5, 6]
>>> x.extend(y)
>>> x
[1, 2, 3, 4, 5, 6]
```

- **index** asks for the index of a specified value.
```python
>>> y = ["one", "two", "three", "four"]
>>> y.index("two")
1
>>> y.index("three")
2
>>> y[3]
'four'
```

- **insert** will add an additional value at a specified index.
```python
>>> x = [1, 2, 3]
>>> x.insert(0, 99)
>>> x
[99, 1, 2, 3]
>>> x.insert(2, 1999)
>>> x
[99, 1, 1999, 2, 3]
```

- **pop** takes in an index and returns that value (removed from list)
```python
>>> x = [1, 2, 3]
>>> x.pop()
3
>>> x
[1, 2]
>>> x.pop()
2
>>> x
[1]
>>> x.pop()
1
>>> x.pop()
[]
>>> x.pop()
IndexError: pop from empty list
>>> x = [1, 2, 3]
>>> y = x.pop(0)
>>> y
1
>>> x
[2, 3]
```

- **remove** will remove a specified value.
```python
>>> y = ["one", "two", "three", "four"]
>>> y.remove("two")
>>> y
['one', 'three', 'four']
```

- **reverse** will inverse a list.
```python
>>> y = ["one", "two", "three", "four"]
>>> y.reverse()
>>> y
['four', 'three', 'two', 'one']
```

- **sort** will sort a list of string alphabetically and a list of numbers numerically. It will permanently alter the only copy.
```python
>>> y = ["one", "two", "three", "four"]
>>> y.sort()
>>> y
['four', 'one', 'three', 'two']
```


### Indexable

Indexable means that you can access a value by calling on the index number (position). You call that index number using `[]` notation. Index always starts at `0`.

For example:
```python
y = ["one", "two"]
y[1], y[2]
```
Will return `'one', 'two'`. `IndexError` will be returned if you call on a index that is out of range. (Sidenote: this is an exploitable feature.)

Essentially, if you can index it, it is ordered. If it is ordered, it is indexable.

### Iterable

Iterable means that you can loop over it. It's not one thing, it's many things. A loop will apply the same function to each of the positions (indices) in a list, i.e., is iterable.

### Mutable

Mutable means that it's changable; immutable means that it is not changable.
A real life example would be like saying your hat is mutable but your head is immutable. 
- A string is immutable.
- A list is mutable.
- An array is mutable.

For example, we can change the list of x by calling upon the index and overwriting it:
```python
x = [1, 2, 3]
x[0] = 99
print(x)
```
Returns `x = [99, 2, 3]`.

`id()` returns the address and memory where that data lives. Think of memory like a post office; it's a bunch of addresses in order.


---
## Tuple

- `()` parenthesis
- ordered
- immutable
- indexable
- iterable


---
## Set

- `{}` curly brackets
- unordered
- distinct (unique
- not indexable
- iterable


---
## Dictionary

- `{}` curly brackets
- ordered (sort of)
- keys are distinct
- always comes in pairs
- not indexable but is searchable
- mutable
- iterable