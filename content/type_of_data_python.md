+++
date = '2025-01-09T20:53:24+03:00'
title = 'Basic data types in Python'
categories = [ "python" ]
+++

#### Integers

The data type for integers is called int (from the English "integer"). Integers can be positive, negative, or zero.

```py
a = 42 # Positive integer
b = -10 # Negative integer
c = 0 # Zero
d = 1234567890 # Large integer
```

#### Floating point numbers

Data type for floating point numbers (fractional numbers) it's called float. These numbers are used to represent real numbers, that is, numbers with a fractional part. Examples: `3.14`, `-0.001`, `2.0`.

```py
a = 3.14 # Positive floating point number
b = -0.001 # Negative floating point
number c = 2.0 # Floating point number, although the value is an integer
d = 1.23e-4 # Scientific notation: 1.23 * 10^(-4) = 0.000123
```

#### Lines

Strings (type str) are sequences of characters used to store and process text data.


```py
s1 = "Hello world!" # String in double quotes
s2 = 'Python'        # A string in single quotes
s3 = """Is
a multiline
string """ # A multiline string in triple quotes
s4 = '123' # A string containing numbers
```

#### Lists

Lists (type list) are ordered mutable collections of elements. Lists can contain elements of different data types (numbers, strings, other lists, etc.), and they are one of the most commonly used data structures.

```py
numbers = [1, 2, 3, 4, 5] # List of integers
fruits = ["apple", "banana", "cherry"] # List of strings
mixed = [1, "apple", 3.14, True]  # A list with different types
of nested items = [[1, 2], [3, 4], [5, 6]]  # Nested list (list of lists)
```

#### Dictionaries

Dictionaries (dict type) are unordered collections of key-value pairs. The keys in the dictionary are unique and are used to access the corresponding values. Dictionaries are very useful for storing and quickly searching data by key.

```py
# Dictionary with key strings
person = {
    "name": "Alexey",
"age": 25,
"city": "Moscow"
}

# Dictionary with different types of keys
mixed_dict = {
    1: "alone",
    "two": 2,
(3, 4): " the motorcade"
}

# Empty dictionary
empty_dict = {}
```

#### Tuples

Tuples (tuple type) are ordered immutable collections of elements. Tuples are similar to lists, but unlike lists, they cannot be changed after creation. This makes them useful for storing data that should not change.

```py
# A tuple of numbers
numbers = (1, 2, 3, 4, 5)

# A tuple of strings
fruits = ("apple", "banana", "cherry")

# Tuple with elements of different types
mixed = (1, "apple", 3.14, True)

# Empty tuple
empty_tuple = ()

# A tuple of one element (don't forget the comma!)
single_element = (42,)
```

#### Sets

Sets (type set) are unordered collections of unique elements. Sets are useful for performing operations such as removing duplicates, checking whether an element belongs to, and mathematical operations on sets (union, intersection, difference, etc.).


```py
# Set of integers
numbers = {1, 2, 3, 4, 5}

# Multiple lines
fruits = {"apple", "banana", "cherry"}

# Set with elements of different types
mixed = {1, "apple", 3.14, True}

# Empty set (use set(), as {} creates an empty dictionary)
empty_set = set()
```

#### Boolean values

Boolean values (type bool) represent Boolean values: True and False. They are used to perform logical operations, control the flow of program execution (for example, in if conditions, while loops), and work with logical expressions.

```py
is_raining = True
is_sunny = False
```