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