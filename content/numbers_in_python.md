+++
date = '2025-01-21T12:00:24+03:00'
title = 'Working with Numbers in Python'
categories = [ "python" ]
+++

Let's go over how basic math operations work in Python.

#### Addition (+)

```python
a = 10
b = 5
result = a + b
print(result)  # Output: 15
```

#### Subtraction (-)

```python
a = 10
b = 5
result = a - b
print(result)  # Output: 5
```

#### Multiplication (*)

```python
a = 10
b = 5
result = a * b
print(result)  # Output: 50
```

In Python, you can multiply an `int` with a `float`. The result will always be a `float`.

This happens because Python automatically converts the integer to a float.

#### Division (/)

Division always returns a floating point number (`float`), even if the result is a whole number.

```python
a = 10
b = 5
result = a / b
print(result)  # Output: 2.0
```

Even `1 / 1` will return `1.0`.

#### Integer Division (//)

Returns only the integer part of the division (truncates the decimal).

```python
a = 10
b = 3
result = a // b
print(result)  # Output: 3
```

#### Modulo (%)

Returns the remainder of a division.

```python
a = 10
b = 3
result = a % b
print(result)  # Output: 1
```

#### Exponentiation (**)

```python
a = 2
b = 3
result = a ** b
print(result)  # Output: 8 (2 raised to the power of 3)
```

#### Shorthand Operations

Python supports shorthand notation for arithmetic operations.

```python
a = 10
a += 5  # Same as a = a + 5
print(a)  # Output: 15

a *= 2  # Same as a = a * 2
print(a)  # Output: 30
```

If at least one of the operands is a floating-point number (`float`), the result will always be a `float`.

This rule applies to all arithmetic operations: addition, subtraction, multiplication, and division.
