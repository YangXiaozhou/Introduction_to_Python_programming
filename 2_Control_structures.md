This is Chapter 2 of the four-part series of Introduction to Python Programming, based on Dr. David Joyner's Edx [course](https://www.edx.org/professional-certificate/introduction-to-python-programming). To see the previous chapter, go here. To see the next chapter, go here. 

[TOC]

# Control structures

Control structures are programming statements that control, in what sequence, a series of code are run. They put some "human logic" in to a block of code. Until now, all the programs that we've written run from top to bottom in a linear sequence. It's easier to interpret and debug. However, the power of programming shows significantly once we add in control structures. For example, control structures we learn next will be able do things like:

- If a pre-specified condition is met, run code block A; If not, run code block B.
- If condition 1, 2, and 3 are all met, run code block A; If condition 1 is met, run code block B; If condition 2 is met, run code block C; if condition 3 and 4 are met, run code block D.
- Repeatedly run the next block of code for 10 time.
- Repeatedly run the next block of code until a pre-specified condition is met.

And many other powerful things. 

## Conditionals

The first kind of control structures is called conditionals. They are statements that control which segment of code is executed based on the result of a condition evaluation. 

In Python, we work with three conditional keywords: `if`, `elif`, `else`.  See the following example of a chained conditional.

```python
Some code here  # Outside if-else block

if <expression_1>:
  Code block A
elif <expression_2>:
  Code block B
elif ...:
  some code
elif ...:
  some code
else:
  Code block C
  
Some code here  # Outside if-else block
```

Notice a few things in the conditional template above:

- Conditional code forms a block by itself. Code above it and below it are not affected by the control logic, i.e., they are not subject to any of the conditional evaluation.
- `if` and `elif` means "if something is true" and "*el*se, *if* something is true". 
-  `<expression>` follows `if` and `elif` to specify what that "something" is. It is a Boolean value or the equivalent of it, e.g., `True`, `10 > 0`, `False`, `True and False`. 
- If `<expression_1>` is not true, the program skips Code block A and continues to the next conditional evaluation.
- `else` means all the previous conditionals are rejected, as a last resort, we'll run Code block C, without evaluating any condition.
- In a chained conditional like the above, at most one block of code is run. Which code block runs depend on the condition evaluation result. 

Besides Boolean evaluations, there are a few special things that are considered as `False` in Python:

- Empty strings: `""`, `''`
- Empty list: `[]`, `()`
- `0`
- Singleton none: `None`

Python supports a shorter way to express single if-else conditional evaluation. Instead of the sequential way above, we can write:

```Python
a_line_of_code if <expression> else another_line_of_code
```
The above code runs `a_line_of_code` if `<expression>` is true. If not, it runs `another_line_of_code`.

## Loops

What if we wish to execute a segment of code repeatedly, e.g., for ten times, or until a condition is met? Loops allow us to do exactly that. There are two Python keywords to construct loops: `for` and `while`. `for` constructs loops where the number of repeats is known; `while` is used when we only know a terminating condition. 

Here's a template for `for` loops:

```python
for i in [1,2,3]:  # For each number i in the list of [1, 2, 3]
		print(i)  
  
# The code above prints
# 1
# 2
# 3
```

And the template for `while` loop:

```python
number = 1
while number <= 3:  # Repeat while number is less than or equal to 3
    print(number)  
    number += 1  

# The code above prints
# 1
# 2
# 3                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     
```

There are some keywords that we can use inside the loop for special control purposes. 
- `continue`: Ignore the rest of the code in this current loop, continue with the next round of execution. 
- `break`: Ignore the rest of the code in the current loop and exit the loop. 
- `pass`: Do nothing, continue with the next iteration in the loop. 

## Functions

The concept of scope

- Scope means the portion of program that a variable can be seen and accessed. 
- Compiled languages are generally different in scope design from scripted languages. 
- Scope is usually defined by control structures.

Scoping in Python: Built-in scope >= global scope >= enclosing scope >= local scope

- Local scope: Variables created inside Python functions.
- Enclosing scope: Not local nor global scope, hence nonlocal scope, e.g. inside one function but outside another.
- Global scope: Variables which can be accessed anywhere in a program.
- Build-in scope: Largest scope, all variable names loaded into Python interpreter, e.g., `print()`, `len()`, `int()`.

Parameter: Variable that functions expect to receive an input.

Argument: Value of the function parameter passed as input.

## Error handling

Exception handling: Structure that anticipates and catches errors to avoid crashing and execute certain code.

Python error handling: 

- `try` - `except` - `else` - `finally`
- `try` to execute this segment of code, `except` some error occurs, then do that instead. `else`, if no error occurred, run this segment of code. `finally`, regardless of the occurrence of errors, run this segment of code. 
- `finally`: segment of code to run no matter what happens above, e.g., closing a file. 

Nested exception-handling structure

- Errors escalate up incrementally to see if they can be caught. 
- Errors also rise through function calls, e.g., an error occurred inside a function. 

---

This is Chapter 2 of the four-part series of Introduction to Python Programming, based on Dr. David Joyner's Edx [course](https://www.edx.org/professional-certificate/introduction-to-python-programming). To see the previous chapter, go here. To see the next chapter, go here. 