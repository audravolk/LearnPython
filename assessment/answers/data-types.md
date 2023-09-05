# Data Types

## Integers

1. *How would you convert a float or a string to an integer?*

Convert a float to an integer using `int()`. 
For example:
```Python
int(5.33335)
```
Returns `5`.

Convert a string to an integer using `int()`.
For example:
```Python
int("string")
```
Returns an error, because a string cannot be converted to an integer. However, if the string represents a valid integer,, it will return the integer within the string. For example, `int("5")` will return `5`. 

---

2. *What does it mean that integers in Python 3 are of arbitrary size?*

The term "arbitrary size" in regards to integers in Python refers to the fact that numbers produced by Python (of almost any size) will be dynamically stored, only limited by the working memory of the computer. This allows the user to specify a wide range of numeric values without having to specify the exact number (as opposed to some other coding languages with fixed-size integers).
For example:
```Python
large_integer = 2 ** 1000
```
Says 2 to the power of 1000, which normally will produce an integer with thousands of decimal places in some other coding languages, but Python will handle it without issues.

---

3. *What is the difference between `//` and `/` when performing division operations in Python?*

`//` performs division and displays an integer (rounding down).
`/` performs division and displays a floating-point number.

---

## Floats (Floating-Point numbers)

1. *How do you round a floating-point number to a specific number of decimal places in Python?*

Convert a floating-point number to a specific number using  `round(number, decimal places)`.
For example:
```Python
number = 3.14159265
rounded_number = round(number, 2)
print(rounded_number)
```
Returns `3.14`.

---

2. *Can you explain the limitations of floating point arithmetic and why it might lead to seemingly odd results (for example, `0.1 + 0.2 != 0.3`)?*

In Python, `0.1 + 0.2 != 0.3` (0.1 + 0.2 is not equal to 0.3), and rather returns `0.30000000000000004` because floating-point arithmetic represents real numbers as binary fractions (decimals). Computers use binary (base-2) while humans use decimal (base-10), so some decimal fractions cannot be represented in binary, and thus will return numbers like the one mentioned above.

---

3. *How would you convert a string or an integer to a float?*

Convert a string to a float using `float()`.  The float will only convert a string to a float where the string contains a valid number.
For example:
```Python
float("3")
```
Returns `3.0`.

Convert an integer to a float using `float()`.
For example :
```Python
float(1)
```
Returns `1.0`.

---

## Complex Numbers

1. *How would you define a complex number in Python?*

A complex number contains a real part plus an imaginary part (for example "2 + 4i"). Imaginary parts are shown by multiplying a number by the variable "i" (i = sqrt(-1)). Imaginary parts are represented in Python by attaching `j` or `J` to the imaginary number.
For example, 4i is represented in Python as `4j`.
```Python
real_number = 2
imaginary_number = 4j
complex_number = real_number + imaginary_number
print(complex_number)
```
Returns `2+4j`.

Python has a constructor to represent complex numbers. Use `complex()` where `()` specifies first the real number, and second the complex number.
For example:
```Python
z1 = complex(2.0,4.0)
print(z1)
```
Returns `2 + 4j`.

---

2. *How can you access the real and imaginary parts of a complex number?*

Us the attributes `.real` and `.imag` following the variable you have defined as a complex number to access the real and imaginary parts.
For example:
```Python
z1 = 2 + 4j
real_part = z1.real
imaginary_part = z1.imaginary
print("Imaginary Part:", imaginary_part)
```
Returns `Imaginary Part: 4.0`.

You can also perform basic operations between complex numbers using `+`, ``-``, ``*``, `/` .

---

## Strings

1. *How do you concatenate two strings?*

Simply add two strings together to concatenate them.
For example:
```Python
string1 = "Hello, "
string2 = "world!"
concatenated_string = string1 + string2
print(concatenated_string)
```
Returns `Hello, world!`

---

2. *What are some methods for formatting strings in Python? Can you give examples of each?*

f-strings are useful for embedding variables, they are represented like `f"()"`. Use curly braces `{}` around variables within the f-string.
For example?
```Python
var_string1 = "Hello, "
var_string2 = "world!"
concatenated_f_string = f"{var_string1}{var_string2}"
print("concatenated_f_string")
```
Returns `Hello, world!`.

---

3. *What is string slicing? Give an example of how you might use it.*

Slice a string by specifying what position to slice the string at. Slicing means to remove. The syntax is `string[start:stop:step]`.  `step` is optional, it means stride size (how many characters to move forward) with default of `1`. 

Slice to extract a substring. Omitting the start index implies starting from the beginning.
For example, while including start index:
```Python
text = "Hello, world!"
substring = text[0:5]
print(substring)
```
Returns `Hello`.
Likewise, while omitting start index:
```Python
text = "Hello, world!"
substring = text[:5]
print(substring)
```
Also returns `Hello`.

Omitting the stop index implicitly goes to the end.
For example:
```Python
text = "Hello, world!"
substring = text[7:]
print(substring)
```
Returns `world!`.

Negative indices count backward from the end to specify splice.
For example:
```Python
text = "Hello, world!"
substring = text[-6:-1]
print(substring)
```
Returns `world`.

Slice with a step value using the third entry.
For example, if we want to start from the beginning, go to the end, and splice every 2nd character:
```Python
text = "Hello, world!"
substring = text[::2]
print(substring)
```
Returns: `Hlo ol!`.

Reverse a string using `[::-1]`.
For example:
```Python
text = "Hello, world!"
substring = text[::-1]
print(substring)
```
Returns `!dlrow ,olleH`.

---

4. *What is the difference between a string’s `find()` and `index()` methods?*

For a given string, these functions will search for a substring and return the index of it's first occurrence. They behave differently when the substring is not found.
- `find()` will return `-1` if not found.
- `index()` returns `ValueError` if not found.

Using `find()`:
```Python
text = "Hello, world!"
index1 = text.find["world"]
print(index1)
```
Returns `7`.

Using `index()`:
```Python
text = "Hello, world!"
index2 = text.index["python"]
print(index2)
```
Returns `ValueError`.

---

5. *What are escape sequences in Python strings, and when might you use them?*

Escape sequences area combination of characters that represent a special character. They begin with a backslash `\` followed by one or more characters. They are used when their characters normally represent something else in Python.
- `\n` represents a break which moves text to the next line.
- `\t` represents a tab which inserts a horizontal tab (whitespace).
- `\\` represents a backslash.
- `\'` and `\"` represent single and double quotes.
- `\xhh` or `\xhhhh` represents a hexadecimal character using its ASCII code.
For example:
```Python
heart_symbol = "\u2665"
print(heart_symbol)
```
Returns `♥`.

---

## Booleans

1. *What values in Python are considered “falsy”?*

`bool()` returns `True` or `False`. "Falsy" are values that are equivalent to `False`. Same concept for "Truthy".
The following values are all considered falsy:
- `bool(False)`
- `bool(0)`, `bool(0.0)`, `bool(0j)`
- Empty sequences and collections: 
	- Empty string`""`
	- Empty dictionary `{}`
	- Empty list `[]`
	- Empty set `set()`
	- Empty tuple `()` or `tuple()`

For example:
```Python
def check_truthiness(value):
    if value:
        print(f"{value} is truthy")
    else:
        print(f"{value} is falsy")

check_truthiness(False)
check_truthiness(None)
check_truthiness(0)
check_truthiness(0.0)
check_truthiness([])
check_truthiness({})
check_truthiness("")
```
Results say for all of these values `is falsy`.

---

2. *What is the difference between `==` and `is` when comparing variables in Python?*

`==` is the Equality Operator. It's used to compare values to check if they are equal.
For example, comparing the contents of "a" and "b" (not their identity):
```Python
a = [1, 2, 3]
b = [1, 2, 3]

result = a == b
print(result)

```
Results in `True`, because the lists have the same content.

`is` is the Identity Operator. It's used to compare the identity or memory address of two variables to check if they refer to the same object.
For example, to see if "a" and "b" are the same object:
```Python
a = [1, 2, 3]
b = a 

result = a is b
print(result)

```
Results in `True` because both variables refer to the same list object.

---

3. *How would you use the `and`, `or`, and `not` Boolean operators in Python?*

`or` operator is used to combine 2+ Boolean expressions. It returns `True` if they are all the same.
Example:
```Python
x = True
y = False

result = x and y
```
Returns `False`.

`and` operator is used to combine 2+ Boolean expressions. It returns `True` if they at least one of the expressions are `True` and `False` if all of the expressions are false.
Example:
```Python
a = True
b = False

result = a or b
```
Results `True`.

`not` operator is used to negate a Boolean expression. It returns the opposite Boolean value.
Example:
```Python
flag = True

result = not flag
```
Results `False`.

Here are some combination examples:
```Python
age = 25
has_license = True

if age >= 18 and has_license:
    print("You can drive!")
```

```Python
is_weekend = True
is_holiday = False

if is_weekend or is_holiday:
    print("It's a good time to relax!")
```

```Python
has_permission = False

if not has_permission:
    print("You don't have permission to access this resource.")
```

---

4. *Can you explain short-circuit evaluation in the context of Boolean operations?*

Short-circuit evaluation is an optimization technique to improve `and` and `or` operators. It evaluates an expression from left to right and stops when the final result is determined, ignoring the rest of the expression.

In the context of Boolean, there may be side effects.
For example, regarding the `and` operator:
```Python
x = False
y = some_function()
result = x and y
bool(result)
```
Results `False` regardless of what `some_function`may be because the right operand `y` is not evaluated.

For example, regarding the `or` operator:
```Python
x = False
y = some_function()
result = x or y
bool(result)
```
Results `False` regardless of what `some_function` may be (even if it could result in `y` being `True`, which would make the result incorrect).

---

_This [link](overview.md) will bring you back to the main assessment._
