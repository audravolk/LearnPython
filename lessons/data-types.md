# Data Types

There are a few primitive data types in Python to focus on.

+ string
+ integer
+ decimal
+ boolean

---

## Strings

A **string**, which is represented by the instance variable name and casting function name `str`, is a data type that is always surrounded by quotes (either double or single) and is an iterable object.

```python
greeting = "Hello, world!"  # this is a string
farewell = 'Goodbye!'  # also a string
```

You can iterate over a string as if it is a container of letters, with each letter occupying a unit of space in an array-like object.

```python
string = "hello"
print(string[0])  # h
print(string[3])  # l
```

You can add strings together. If you add one string to another, you will concatenate the second string on to the end of the first string.

```python
prefix = "hello"
suffix = "world"
print(prefix + suffix)  # helloworld
```

---

## Integers

In Python, the **integer**, which is represented by the instance variable name and casting function name `int`, data type is a whole number (positive or negative) without any surrounding enclosing symbols.

```python
number_a = 500  # this is an int
number_b = -25  # this is also an int
number_c = 1_000_000  # this is still an int
```

You can add, subtract, multiply, divide, and perform many other arithmetic operations to integers as well as mix operations with decimal value types.

```python
number_a = 20
number_b = 4
print(number_a + number_b)  # 24
print(number_a - number_b)  # 16
print(number_a * number_b)  # 80
print(number_a / number_b)  # 5.0
print(number_a // number_b)  # 5
print(number_b ** 3)  # 64
print(number_a + 3.5)  # 23.5
```

---

## Decimals

In Python, the **decimal**, which is represented by the instance variable name and casting function name `float`, data type is a decimal value (positive or negative) without any surrounding enclosing symbols.

```python
number_a = 500.0  # this is a float
number_b = -25.0  # this is also a float
```

You can add, subtract, multiply, divide, and perform many other arithmetic operations to decimals as well as mix operations with integer value types.

```python
number_a = 20.0
number_b = 4.0
print(number_a + number_b)  # 24.0
print(number_a - number_b)  # 16.0
print(number_a * number_b)  # 80.0
print(number_a / number_b)  # 5.0
print(number_a // number_b)  # 5.0
print(number_b ** 3)  # 64.0
print(number_a + 3)  # 23.0
```

---

## Boolean

In Python, the **boolean**, which is represented by the instance variable name and casting function name `bool`, data type is a binary (true or false) value.

```python
bool_a = True
bool_b = False
```
