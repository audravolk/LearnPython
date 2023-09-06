
### type

`type()` will return the type of data in the parenthesis.

For example, you can make an empty list with the syntax `x = []`; and ask what type is `x`?
```python
x = []
type(x)
```
Returns `list`. `type()` tells you the type of object.

For example:
```python
x = 1
y = "hello"
type(x), type(y)
```
Returns `(int, str)`.

### dir

`dir()` will return a list of instance methods that `()` can do.

For example: show me the methods that `x` can do:
```python
dir(x)
```
Returns a description of `x` and all of things (verbs) that `x` can do.

### help

`help()` will return helpful info.

For example:
```python
help(X)
```
Returns a "less pipe" also entering `| less`. 

A less pipe is like a text viewer. 
- You can search for things in the output in the command line.
- You can also use `| more`. They are essentially the same thing.
- Lets you use arrow keys instead of you mouse.
- Press `q` to get out of the pipe.
