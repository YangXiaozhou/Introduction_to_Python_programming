# Fundamentals and procedural programming

## Computing

### Computing vs programming

- Computing is loosely anything we do that involves computers.
- Programming is the act of giving a set of instructions for computers to act on.
- Computing is about what we want to do with computers using the programming language that we learnt.

### Programming vocabulary

Program and code

- A line of code: generally the smallest unit of programming that instructs computer to do something.
- Program: a set of lines of code that usually serve one overall function. 

Input and output

- Input: what a program takes in to work on.
- Output: what a program produces in return.

Compiling and executing

- Compiling: compilers look for syntax errors in our code, like proofreading an article.
- Executing: actually running the program written. 

Programming languages

- To write computer programs, we need to learn programming languages, like learning to write.
- Languages differ in many ways, it's important to keep in mind the language spectrum.
    - Static and compiled vs dynamic and interpreted. 
    - Execute one line at a time rather than script-based

Console vs graphical user interface (GUI)

- We interact with computer programs through interfaces, like Terminal and Words.
- To focus our learning on computing, we start with text-based input and output.
    - Console: command-line interface that is solely based on text.
    - GUI: much more complex and commonly used interface of computer programs.

## Introduction to Python

Created in 1990s, became popular in 2000s, one of the most popular today. Python is a high-level language: 

- abstracts aways from core processor and memory
- more portable across different operating systems

Python is also an interpreted language:

- run code line-by-line without trying to compile it first

### Programming

Programming flow: Writing code --> Running code --> Evaluating results --> Repeat

- Chaining together instructions through lines of code
- `print()` function
- Work in small chunks

### First Python program: Hello, world. 

- `print` is in lower case
- the message to be printed is enclosed by parenthesis
- the actual message to be printed is in quotation marks

### Compiling vs executing

Using the analogy of building a table with parts and instructions

Compiling

- Practically, this process looks over our code to see if everything makes sense. 

- Technically, it also translates our code into lower-level machine-understandable code. 

- Compiling before running is not required for every language.
    - Static or compiled: C, Java
    - Dynamic or interpreted: Python, JavaScript

Executing

- Actually running the code and letting it do when we want it to do.

- Three scenarios can happen:
    - Run into errors
    - Did not do what we intend it to do
    - Run as intended

### Evaluating results

- Correct results: we're happy. Move on.

- Errors: locate and correct them.
    - Error example: for i within range(1, 9): print(i)
    - Demonstrate features of encountering error in Python

- Incorrect results: locate and revise. 
    - Code example: print 1 to 9 instead of 1 to 10. 

## Debugging

What is debugging?

Debugging is trying to find why your code doesn't behave the way you want it to. It is also like doing research on our code; the aim is to gather as much information as necessary to debug.

![debugging](/Users/frs/Downloads/2_Data_science/0_Foundation/4_Computer_science/Introduction_to_Python_programming/assets/debugging.gif)

![debugging](/Users/frs/Downloads/2_Data_science/0_Foundation/4_Computer_science/Introduction_to_Python_programming/assets/debugging2.png)

Types of errors:

- Compilation errors: e.g., syntax error, name error, type error
- Runtime error, e.g., divide by zero error, null error, memory error
- Semantic error, .e.g, incorrect code logic

Common errors in Python: 

- `NameError`: using a variable that does not exist
- `TypeError`: doing something that does not make sense for the type of variable
- `AttributeError`: using attribute of some type of variable which does not make sense
- `SyntaxError`: catch-all name for all sorts of invalid syntax errors in Python

### Basic debugging

- Print debugging/tracing

- - Print out the status of the code throughout the run process

- Scope debugging

- - Debug on the basis of small sections of code

- Rubber duck debugging

- - Explaining in detail the logic, goal, and operations of the code to a third person/object

### Advanced debugging:

- Step-by-step execution
- Variable visualization: real-time monitoring of variable values
- In-line debugging: automatic checking of errors while writing the code

Additional resource: 

- The [Testing and Debugging lecture](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-00-introduction-to-computer-science-and-programming-fall-2008/video-lectures/lecture-11/) from MIT OpenCourseware's Introduction to Computer Science and Programming.

## Procedural programming

Here are four of the most common programming paradigms:

- Procedural programming: giving instructions to the computer to carry out in order
- Functional programming: programs based on functions/methods with inputs and outputs
- Object-oriented programming: programs with custom data types that have custom methods to express complex concepts
- Event-driven programming: programs which await and react to events rather than running code linearly

Comments and documentation:

- In-line comment: alongside lines of code, to explain the specific line of code
- Code-block comment: before segments of code, to explain what the segment of code does

## Variables

What is a variable?

- A name that holds some value
- Central to programming, holds information
- Can contain more than just number: integer, float, string, date, Boolean, and etc.

Common data types in Python

- `int`: integer
- `float`: floating point number
- `str`: a string of characters
- `bool`: Boolean

Type conversion in Python:

- `int()`
- `float()`
- `str()`
- `bool()`

## Logical operators

Operators: Simplest ways to act on data, mostly on basic data types

- Mathematical operators: perform mathematical operations, commonly known but not very useful in programming
- Logical operators: perform logical judgements, less known but play bigger role in programming

Logical operators

- Relational operators: `<`, `>`, `>=`, `<=`, `==`, `in` (set operator)

- Boolean operators: `not`, `and`, `or`

- - Order of evaluation: `not` > `and` > `or`

Truth table: A table that maps out the Boolean values of a statement in Boolean logic, based on the value of the individual Boolean variables

## Relational operators

Mathematical operators: `+`, `-`, `/`, `*`, `%` (remainder), `//` (floor), `**` (exponentiation)

Assignment operator: `=`

- Assign value to a variable

- Self-assignment, e.g., `+=`, `*=`: assign a new value based on the variable's current value

- Incrementing: increment the value of a variable, typically by one

- - `num = num + 1` is equivalent to `num += 1`
        - `num = num / 3` is equivalent to `num /= 3`

Operators on strings:

- Strings work with: `+`, `*`, `<`, `>`, `==`, `<=`, `>=`.
- Relational comparison is done on the order of their appearance.

# Control structures

- Conditionals: Statement that control which segment of code is executed.
- Loops: Structure that executes a segment of code multiple times.
- Exception handling: Structure that anticipates and catches errors to avoid crashing and execute certain code.

## Conditionals

What are considered *False* in Python:

- Empty strings: `""`, `''`
- `0`
- Empty list: `[]`, `()`
- Singleton: `None`

## Loops

- Zero-based indexing
    - Legacy reason, in earlier primitive languages, variable pointers point to the first element in a list. Thus index then means how many items to skip to reach the target item, e.g. to get 5th item, we need to skip 4 items. 
- Special key words used in loop body:
    - `continue`: Ignore the rest of the code in this current loop, continue with the next round of execution. 
    - `break`: Ignore the rest of the code in this current loop and exit the loop. 
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

Python error handling: 

- `try` - `except` - `else` - `finally`
- `try` to execute this segment of code, `except` some error occurs, then do that instead. `else`, if no error occurred, run this segment of code. `finally`, regardless of the occurrence of errors, run this segment of code. 
- `finally`: segment of code to run no matter what happens above, e.g., closing a file. 

Nested exception-handling structure

- Errors escalate up incrementally to see if they can be caught. 
- Errors also rise through function calls, e.g., an error occurred inside a function. 

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

# Objects and algorithms

This chapter introduces us to two fundamental pillars of knowledge in computer science: object-oriented programming (OOP) and algorithms. Breadth over depth is emphasized in this chapter. 

## Objects

### What are objects?

Objects are concepts from OOP paradigm. 

- OOP is a paradigm, in contrast to, e.g., procedural and functional programming, where custom data types are defined and used with custom methods defined for them. 
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



