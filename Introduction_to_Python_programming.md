This is a four-part series of Introduction to Python Programming, based on Dr. David Joyner's Edx [course](https://www.edx.org/professional-certificate/introduction-to-python-programming). To see my review of the course, go here. To see the next Chapter, go here. 

[TOC]

# Fundamentals and procedural programming

## Computing

First up, is computing and programming the same thing?

Computing is loosely anything we do that involves computers. Programming is the act of giving a set of instructions for computers to act on. Computing is about what we want to do with computers using the programming language that we learnt.

Here are some commonly used programming vocabularies to distinguish:

- Program vs code
    - Program: A set of lines of code that usually serve one overall function. 
    - A line of code: The smallest unit of programming that instructs computer to do something.
- Input vs output
    - Input: What a program takes in to work with.
    - Output: What a program produces in return.
- Compiling vs executing
    - Compiling: Compilers look for syntax errors in our code, like proofreading an article.
    - Executing: Actually running the program written. 
- Console vs graphical user interface (GUI):
    - Console: Command-line interface that is solely based on text input and output, e.g., Terminal on Mac.
    - GUI: Much more complex and commonly used interface of computer programs, e.g., Microsoft Word. 

What are programming languages?

To be able to write Japanese essays, we need to learn Japanese, Similarly, to write computer programs, we need to learn programming languages. However, languages differ in many ways, it's important to keep in mind the [language spectrum](https://www.realpythonproject.com/you-need-to-know-compiled-interpreted-static-dynamic-and-strong-weak-typing/).

- Static and compiled: e.g., C, C++, Java. These languages do not allow variable type changes after declaration. The program is translated into machine-readable code at once. 
- Dynamic and interpreted: e.g., Python, JavaScript. These languages allow dynamically changing variable types. The program is translated into machine-readable code one line at a time.

## Introduction to Python

Python was created in the 90s, became popular in 2000s. It is one of the most popular languages today. It is a high-level language in the sense that it abstracts aways from core computer processor and memory and is more portable across different operating systems. It is also an interpreted language as it runs code line by line without trying to compile the whole program first.

**Python programming**

The common work flow of programming is: Writing code --> Running code --> Evaluating results --> Repeat. Multiple instructions are chained together through lines of code. When we wish to see the value of a variable or the result of a program, `print()` function is usually used. Also, it is recommended to work in small chunks of code at a time for Python programming. 

**First Python program: Hello, world!** 

We wish to write a program that outputs a message, "Hello, world!". Note that `print` is in lower case. Also, the message to be printed is enclosed by parenthesis

**Compiling vs executing**

The difference between compiling and executing a program can be understood through the analogy of building a table with parts and instructions. Compiling means reading the instructions to make sure every parts are in place and the instructions make sense. Executing means actually building the table with the instructions. 

*Compiling*: Practically, this process looks over our code to see if everything makes sense. Technically, it also translates our code into lower-level machine-understandable code. Compiling before running is not required for every language, .e.g., interpreted languages like Python and JavaScript.

*Executing*: Actually running the code and letting it do when we want it to do.

**Evaluating results**

After executing our program, three scenarios can happen:

- Run as intended.
- Did not do what we intend it to do.
- Run into errors.

In the first case, we obtain correct results and we're happy. In the second case, the program executes successfully but produces incorrect results, e.g., instead of printing 1 to 10, it prints 1 to 9. In this case, we need to locate the code that causes the error and revise it. Finally, the program runs into errors and aborts right away. In another words, our program crashes. We need to locate the error-causing code and correct them.

## Debugging

What is debugging?

When our program causes error or produces incorrect results, we want to do debugging. Debugging is the process of finding out why our code doesn't behave the way we want it to. It is also like doing research on our code; the aim is to gather as much information as necessary to debug.

Debugging sometimes is like 

![debugging](/Users/frs/Downloads/2_Data_science/0_Foundation/4_Computer_science/Introduction_to_Python_programming/assets/debugging.gif) 

or like 

![debugging](/Users/frs/Downloads/2_Data_science/0_Foundation/4_Computer_science/Introduction_to_Python_programming/assets/debugging2.png)



### Error types and common errors

There are three types of errors with which we need to debug. We can still think of them in terms of building a table from instructions.

- Compilation errors: These are the errors when we say: "The instructions do not make sense." For example, the code syntax is incorrect (syntax error).
- Runtime error: These are errors encountered when we are building the table/running the code. For example, if one line of code tries to divide by zero, it would cause divide-by-zero error. 
- Semantic error: If the table is successfully built but perhaps with reversed tabletop surface, we've encountered semantic error. For example, an incorrect code logic might not crash the program but produces an incorrect result. 

Here are four commonly encountered errors in Python: 

- `NameError`: Using a variable that does not exist.
- `TypeError`: Doing something that does not make sense for the type of variable.
- `AttributeError`: Using attribute of some type of variable which does not make sense.
- `SyntaxError`: A catch-all name for all sorts of syntax errors in Python.

### Basic debugging techniques

Here are some basic debugging techniques that people use frequently.

- Print debugging/tracing: Printing out the status of the code throughout the program to identify which part is not running as expected.
- Scope debugging: Debugging incrementally on the basis of small sections of code. 
- Rubber duck debugging: Explaining in detail the logic, goal, and operations of the code to a third person/object (e.g., a rubber duck).


### Advanced debugging techniques

In some modern integrated development environments (IDEs), more advanced debugging support is provided.

- Step-by-step execution: The program is run one line at a time, stopping anywhere we wish. 
- Variable visualization: We could also visualize all active variables as the program runs. 
- In-line debugging: Automatic checking of errors is done while we're writing the code.

To learn more about testing and debugging our code, check out the [Testing and Debugging lecture](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-00-introduction-to-computer-science-and-programming-fall-2008/video-lectures/lecture-11/) from MIT OpenCourseware's Introduction to Computer Science and Programming.

## Procedural programming

There are different programming paradigms to use when we write code for a program. Here are four common paradigms:

- Procedural programming: Giving lines of instructions to the computer to carry out in order.
- Functional programming: Writing programs based on functions/methods with inputs and outputs.
- Object-oriented programming: Writing programs with custom data types that have custom methods to express complex concepts.
- Event-driven programming: Writing programs which wait and react to events rather than running code linearly.

In this course, we start with procedural programming, then functional programming. In the last Chapter, we introduce objected-oriented programming. 

Another important part of the code that we write is not computer code but comments and documentation. They are there to help future us and others understand the code so that future improvements can be made. There are mainly two kinds of comments.

- In-line comment: Alongside lines of code, to explain the specific line of code.
- Code-block comment: before segments of code, to explain what the segment of code does.

## Variables

What is a variable?

It is a name in our program that holds some value. Variables are central to programming; Like variables in mathematics, they hold pieces of information. However, variables in computer programs can contain numbers and other things, e.g., characters, list of things, `True`/`False` values. The type of the value is called data type, e.g., `3` is an integer. We use `type(a_variable)` to access the type of `a_variable`.

Here are four basic data types in Python.

- `int`: Integer, e.g., `1`, `10`, `-100`.
- `float`: Floating point number, e.g., `0.3`, `-1000.0`.
- `str`: A string of characters, e.g., `'a'`, `'a & b'`, `'word'`, `'A sentence is also a string.'`.
- `bool`: Boolean variable, e.g., `True`, `False`.

If possible, we could also convert data between different types. Here are the functions to do it in Python.

- `int()`
- `float()`
- `str()`
- `bool()`

## Operators

Operators are the simplest ways to act on data, mostly on basic data types introduced above. There are two types of operators.

- Mathematical operators: Perform mathematical operations, e.g., `+`, `-`. They are commonly known but not the most useful in programming.
- Logical operators: Perform logical judgements, e.g., `>`, `<`. They are less known but play a bigger role in programming.

Logical operators can be further broken down into relational (larger, smaller) and boolean (true, false) operators. 

### Mathematical operators

Most of us are familiar with mathematical operators:

- `+`, `-`, `/`, `*`, 
- `%` (remainder), `//` (floor division), `**` (exponentiation)

A special meaning is attached to the equal sign `=`: Assignment operator. We use `=` to assign value to a variable.

- Normal assignment: The format is `a_variable = a_value`, e.g., `a = 3`. 
- Self-assignment: A Python way of assigning a new value to a variable based on the variable's current value, e.g., `+=`, `*=`.
    - `number = number + 1` is equivalent to `number += 1```
    - `number = number / 3` is equivalent to `number /= 3`

### Relational operators

Unlike mathematical operators, we always receive Boolean values (`True` or `False`) as answers when using logical operators. There are two specific types of logical operators: relational and Boolean.

- Relational operators: `<`, `>`, `>=`, `<=`, `==`, `in`.

Relational operators compare the two sides and ask questions like: is the left hand side larger/smaller/equal to the right hand side? Specifically, `==` is asking whether the two things are equal; `in` is asking whether the left hand side is an element in the right hand side (e.g., if `a` $\in$ `[a, b, c]`). 

There are some operators that work on strings as well. For example, relational comparison of two strings is done based on the order of their constituent characters, e.g., `'abc > bac'` would produce `False` since the position of `a` is before `b`.

- Strings work with: `+`, `*`, `<`, `>`, `==`, `<=`, `>=`.
    - `+` concatenates two strings; `*` duplicates a string by an integer.

### Boolean operators

Another kind of logical operators is Boolean operators. They act on Boolean values and also return Boolean values.

The are `not`, `and`, `or`:

- `not`: Flips the Boolean value that follows `not`.
- `and`: Only returns `True` if both sides are true.
- `or`: Returns `True` when at least one side is true.

For example, `not True` would produce `False`; `True and False` would produce `False`; `True or False` would produce `True`. Sometimes we encounter a long chain of Boolean evaluation. Python has an internal order of evaluation: `not` > `and` > `or`.

---

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
    Some code
elif ...:
    Some code
else:
    Code block C
  
Some code here  # Outside if-else block
```

Notice a few things in the conditional template above:

- Conditional code forms a block by itself. Code above it and below it are not affected by the control logic, i.e., they are not subject to any of the conditional evaluation.
- `if` and `elif` means "if something is true" and "*el*se, *if* something is true". 
- `<expression>` follows `if` and `elif` to specify what that "something" is. It is a Boolean value or the equivalent of it, e.g., `True`, `10 > 0`, `False`, `True and False`. 
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

Function is a block of of related code grouped together to perform a specific task. They replace repetitive codes with a simple line of function call. They help to make our program concise and organized. Functions can be built-in by a language or used-defined.

**An example**

```python
# Define a function
def function_name(a, b=10, *args, **kwargs):
		"""Add a, b, and other things in args."""
    c = a + b
  	
    for arg in args:
      c += arg
    
    return c
  
# Calling(using) a function
function_name(a=100, [1, 2, 3])  # b has a default value of 10.
```

The above is an example of defining a function in Python:

- The function is declared using the keyword `def` followed by the function name that we give it.
- A function can take as many arguments as necessary separated by comma.
- Functions docstring using `"""` details what the function does and how to use it.
- The function returns some value through the keyword `return`.

**Types of arguments**

There are four different types of arguments that we can define in a Python function.

- Keyword arguments: They do not have pre-assigned values in the function definition. While calling a function, these positional arguments have to be given values in their order of appearance. For example, `a` in the above example is such an argument.
- Default arguments: They are arguments which are given default values during function definition. Hence, it may not be necessary to given these values when calling the function. For example, `b` in the above example is such an argument.
- Variable-length arguments
- These are lists of arguments which we do not known in advance how long they are. They are defined in the function definition using *args. 

**The concept of scope**

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

# Data structures

## Data structures

### Passing by value vs passing by reference:

By value: Giving variable values to functions. Functions can can't change the original value.

By reference: Giving variable references to functions. Functions can access and change the original value.

### Passing by value vs passing by reference in Python

Different languages have different ways of differentiating these two types.

- C: variableName (value) vs *variableName (reference)
- Java: primitive types (value) vs non-primitive types (reference) 

Python seems to handle everything via pass-by-value. 

- However, not all types of data are passed by value, e.g., integers, strings.
- The key to discern Python's behavior is: Mutability of the data type. 

### Mutability in Python

Mutability: Whether or not a variable's value can change after being declared.  

In general, all variables in Python are passed by reference. However, only values of mutable data types can be changed, e.g., `list`, `set`, and `dict`. Immutable data types in Python include: `int`, `float`, `tuple`, `bool`, and `str`. 

How Python actually work for immutable data types?

- `my_int = 5`: Python grabs a memory spot and stores '5' in that spot. `my_int` is asked to point to that memory spot with `id(my_int)`. 
- `my_int_2 = my_int`: Python asks `my_int_2` point to the same memory spot as `my_int`.
- `my_int_2 = my_int_2 + 1`: Python creates a new value '6' and grabs a new memory spot to store it. Then it asks `my_int_2` point to the new memory spot as '6' is an immutable data type. 

Basically, for immutable data types, when Python is asked to change its value, it does not change it on the spot. It stores the new value at a new memory location and asks the variable point to the new location instead. Therefore:

- Identical values have identical memory address for immutable data types.
- Each new variable has a new memory address for mutable data types, regardless of the value. 

## Strings

### What are strings?

Some relevant concepts:

- String: A data structure that holds a list, or string of characters, e.g., `"Hello world!"`.
- Character: A single letter, number, symbol, or special character, e.g., `"$"`.
- Unicode: A computing industry standard that sets the correspondence between hexadecimal codes and characters, e.g., `U+0024` means `$`.
- Special characters in programming: new line character, tab, etc.

The true complexity lies in trying to teach computers that way we human view and use these strings of characters. For example, how do we teach computers the concepts of

- Ordering: `'A' < 'B'`, `'Aa' < 'Ab'`. 
- Capitalization: To capitalize a sentence means `"Do this instead"` ->  `"Do This Instead".`
- Cases: Recognize different cases, and conversion between different cases.

### Declaring strings in Python

Python seeks the start and end of the string by matching `'`, `"`, or `'''` characters:

- A normal string: `a = "a string"` or `a = 'a string'`
- A string with quotation: `a = "'a string'"` or `a = '"a string"'`
- A string with double quotation: `a = ''' " 'a string' " '''`

However, we would run into trouble if we wish to declare special characters such as the new line character `\n` or the tab character `\t`. The trick is to use `\` as the escape character. It tells the computer to treat these special characters as normal, e.g, `'\\n'`, `'\\t'`. 

### String concatenation and slicing in Python

Two of the commonly used operations on strings are concatenation and slicing. 

Concatenation: Put two or more strings together to form a new one.

- `my_string_1 + my_string_2`
- `"a string" + my_string_1`
- `my_string_1 += my_string_2`

Slicing: Obtain substrings from a string in Python.

- Using single index: `[index]`
    - `[0]` gets the first, `[-1]`gets the last, and `[i]` gets the (i+1)th character.
    - Zero-based indexing: In early computing age, a variable name points to the first item in the string/list. The index means "how many items do I skip in order to get the target item", e.g., `[3]` says skipping three items from the first item, i.e., to obtain the fourth item. 
    - Zero-based indexing
        - Legacy reason, in earlier primitive languages, variable pointers point to the first element in a list. Thus index then means how many items to skip to reach the target item, e.g. to get 5th item, we need to skip 4 items. 
- Using index range: `[start:end]`, `[start:]`, `[:end]`, `[start:end:space]`
    - Start from the item at index `start` and get a substring with length `end - start`. 
    - Use `space` to get alternate characters, e.g. `[::2]` gets all items at even index. 
- Using negative index
    - `[-n:]`: Starts from the $n$th item from the end.
    - `[:-n]`: Ends at the $n$th item from the end.

### String searching

Another commonly used operation is searching a certain substring in another string. For example, we would like to know if `my_string_1` is contained in `my_string_2`. 

- Using Python keyword `in` and `not in` for a boolean answer.
    - `'David' in "Today is David's birthday"` would give `True`
    - `'star' not in 'A lot of stairs' ` would also give `True`
- Using `find()`: A method defined for the string data type, e.g., `my_string_1.find('star')`.
    - Find the index of the first instance of the substring. If not found, `-1` is returned.
    - We could specify the start and end of the original string to conduct the search.
- Using `count()`
    - Count the number of times a substring is found in a string.

### Useful string methods in Python

There are some other useful methods that we could use on strings in Python.

- `split(separator)`: Split a string into a list of substrings using the separator.
- Case conversion: Convert a string to a different case.
    - `capitalize()`
    - `lower()`
    - `upper()`
    - `title()`
- `strip()`: Strip out all white spaces in a string.
- `replace(old, new)`: Replace all `old` substrings with `new` substrings in a string.
- `"-".join(a_list)`: Use "-" to join all string items in a list and form a new string. 

## List-list structures

A type of data structure that holds multiple individual values under one variable name, accessed by numeric indices. Examples in Python include tuple, e.g., `(1,2,'cat',6)`, and list, e.g., `['a', 2, 'b']`.

- Tuple: An immutable form of list-like structure.
- List: A mutable form of list-like structure. 

Both of them support holding non-homogenous data types, e.g., a tuple has both integers and strings.

### Tuples in Python

There are two ways which we can use to access items in a tuple:

- Using index: Exactly like how we use indices to access substrings in strings.
- Using unpacking technique: `(a, b, c, d) = a_tuple`. 

Usefulness of tuple: Return multiple items from a function, e.g., `return (a,b,c,d)`. 

### Lists in Python

Lists are much more commonly used in Python programming. All the things that work with tuples as mention previously work with lists. The big difference is that lists are mutable. Hence we can do all sorts of operations on lists. For example, here are some common ones:

- `a_list.sort()`: Sort the items in `a_list`, default in ascending order. 
- `a_list.reverse()`: Reverse the order of the items.
- `del a_list[i:j]`: Delete `j-i` items from `a_list ` starting from index `i`.
- `a_list.remove(x)`: Delete item `x` from `a_list`.
- `a_list[i] = x`: Assignment value of `x` to the list item at index `i`.

### Advanced list-like structures

There are more types of list-like structures that have specific advantage for certain applications. They are usually lists with certain restrictions on how items can be accessed or modified. 

- Stacks
    - Only the most recently added item can be accessed. Each subsequent item is accessed by  removing the next recently added one. In inventory management language, it's called first in last out, like stacks of finished goods.
    - One example is the code execution sequence in procedural programming. 
- Queues
    - Items added first are accessed first. Each subsequent item is accessed by removing the previous one. This is also called first in first out, like queues of customers. 
- Linked-lists
    - Linked-lists are different from other lists where each item has an index and can be accessed via a sequence of indices. 
    - The location of an item in a linked-list is only contained in the previous item in the list. 

## File input and output

If we want to have some data of our program persist even after the session ends, we need a way to store and read data from our program.  File input and output are complementary processes of saving data to a file and loading data from a file. A file's encoding specifies a set of rules about writing data to that file and loading data from it. In the most basic form, we would concentrate on dealing with text (`.txt`) files. 

### Reading, writing, and appending

The basic flow of interacting with files involve:

1. Opening a file and assign it to a variable.
2. Do whatever operations we want with the file, e.g., reading data from it, writing data to it.
3. Close the file after we are done.

To open and close files in Python, we use these functions:

- `file = open(file_name, mode)`: `file_name` is the address of the write and `mode ` is one of the three described below.
- `file.close()`: Closing the file after we're done with our operations.

When we open the file in a program, we usually specify a mode of interaction. There are three modes:

- Reading, `r`: It means that we are only reading the file and do not intend to modify it.
- Writing, `w`: We are going to erase everything on it and write some new data into it.
- Appending, `a`: We are going to append some new data to whatever content the file already has.

It's important to specify the mode. Also, opening a file prevents other programs from modifying it. That's why we need to close it too after we're done. 

### Writing files in Python

Basic functions involved in writing data to files:

- `file.write()`: Write one string of text into the file.
- `file.writelines()`: Write a collection of items into the file.
- `print(text, file = file_name)`: This is equivalent to writing `text + '\n'` to the file.

### Reading files in Python

The reverse process of writing data to a file is reading it from a file. By default, Python treats contents read from a file as text. We would need to convert them to other types if needed. Here are some basic functions of reading from a file:

- `file.readline()`: Read the content of a line in the file until the start of the next line.
- `file.readlines()`: Read the content of the file line by line and store them in a list of strings.
- `file.read().splitlines()`: Read the content of the file and split the content into a list of strings using new line character.

## Dictionaries

Dictionary is one of many powerful data structures. It is a data structure that holds multiple key-value pairs where keys can be used to look up corresponding values. The idea of dictionary is common in different programming languages. They are similarly known as maps, associative arrays, hashmaps, or hashtables. In dictionary, there's a one-to-one correspondence between a key and a value. Notably, the order of the collection of key-value pairs do not matter in a dictionary, unlike lists. 

### Dictionaries in Python

While strings are declared with `""` and lists are declared with `[]`, dictionaries are declared with `{}` in Python. For example, a simple dictionary with two arbitrary keys and values can be declared as

- `a_dict = {key_1: value_1; key_2: value_2}`

Python requires that dictionary keys have to be an immutable data type such as string or integer. However, dictionaries themselves are mutable. Hence, we can perform various operations on the values of items in a dictionary, via their keys:

- Modifying a value: `a_dict[key] = new_value`
- Adding a new item: `a_dict[new_key] = new_value`
- Deleting an item: `del a_dict[key]`
- Checking the presence of an item: `a_key in a_dict`

Another important operation that we often use is traversing through items in a dictionary. We can do so in three common ways:

- `for key in a_dict.keys()`: Go through the list of keys.
- `for value in a_dict.values()`: Go through the list of values.
- `for (key, value) in a_dict.items()`: Go through the list of (key, value) pairs.

---

# Objects and algorithms

This chapter introduces us to two fundamental pillars of knowledge in computer science: object-oriented programming (OOP) and algorithms. Breadth over depth is emphasized in this chapter. 

## Objects

### What are objects?

Objects are concepts from OOP paradigm. 

- In contrast to procedural or functional programming, OOP is a paradigm where custom data types are defined and used with custom methods defined for them. 
- Class: We usually refer to such a data type as a class with custom methods and variables (also known as class attributes). 
- Objects and instances: An object or instance is what we usually refer to a particular "variable" created from a class. For example:
    - From a `person` class, we can create a particular person, e.g., `David` or `Mary`.
    - From a `book` class, we can create a particular book, e.g., `book_A` or `book_B`.

Therefore, to understand the class-instance relationship, we can think of the relationship between an unfilled form and a filled one: An unfilled form represents a template, a class; The form can then be filled with different information by different people to create different instances. 

### Objects and instances in Python

Just like how we need to declare a function before using it, to work with objects and instances, we first need to declare the class. Declaring classes in Python is essentially teaching the computer what kind of concepts make sense for the class object. For example

- To make a `book` class, each book instance could have a title, an author, a publication date, etc.
- To make a `person` class, each person instance could have a name, an age, an eye color, etc.

During declaration, Python uses the dot syntax `self.` to assign or access its attributes such as title or author. 

- For example, to set a book instance's name as `'Python Programming'`, we can write: `self.name = 'Python Programming'`. 

### Encapsulating methods in classes



## Algorithms

