This is Chapter 1 of the four-part series of Introduction to Python Programming, based on Dr. David Joyner's Edx [course](https://www.edx.org/professional-certificate/introduction-to-python-programming). To see my review of the course, go here. To see the next Chapter, go here. 

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

### Python programming

The common work flow of programming is: Writing code --> Running code --> Evaluating results --> Repeat. Multiple instructions are chained together through lines of code. When we wish to see the value of a variable or the result of a program, `print()` function is usually used. Also, it is recommended to work in small chunks of code at a time for Python programming. 

#### First Python program: Hello, world! 

We wish to write a program that outputs a message, "Hello, world!". Note that `print` is in lower case. Also, the message to be printed is enclosed by parenthesis

#### Compiling vs executing

The difference between compiling and executing a program can be understood through the analogy of building a table with parts and instructions. Compiling means reading the instructions to make sure every parts are in place and the instructions make sense. Executing means actually building the table with the instructions. 

*Compiling*: Practically, this process looks over our code to see if everything makes sense. Technically, it also translates our code into lower-level machine-understandable code. Compiling before running is not required for every language, .e.g., interpreted languages like Python and JavaScript.

*Executing*: Actually running the code and letting it do when we want it to do.

#### Evaluating results

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

This is Chapter 1 of the four-part series of Introduction to Python Programming, based on Dr. David Joyner's Edx [course](https://www.edx.org/professional-certificate/introduction-to-python-programming). To see my review of the course, go here. To see the next Chapter, go here. 