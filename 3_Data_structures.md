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