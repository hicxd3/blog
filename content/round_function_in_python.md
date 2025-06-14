+++
date = '2025-01-21T12:05:24+03:00'
title = 'round() function in Python'
categories = [ "python" ]
+++

### Number

The `round()` function in Python is used to round numbers. It can round both integers and floating-point numbers.

Syntax of the function `round()`
```python
round(number, ndigits)
```

>`number` — the number to round up

>`ndigits' (optional) — the number of decimal places. If not specified, the number is rounded to the nearest integer.

Rounding to the nearest integer

```python
result = round(3.14159)
print(result) # Output: 3
```

Rounding with the number of decimal places

```python
result = round(3.14159, 2)
print(result) # Output: 3.14
```

Rounding to the nearest larger integer

```python
result = round(3.7)
print(result) # Output: 4
```

Rounding up negative numbers

```python
result = round(-2.7)
print(result) # Output: -3
```

Rounding to the nearest even number
if the number is exactly in the middle

```python
result = round(2.5)
print(result) # Output: 2
```

If `ndigits' is not specified, `round()` rounds to the nearest integer.

If `ndigits` is specified, rounding occurs to the specified number of decimal places.

If the number is exactly in the middle between two possible variants (for example, 2.5), Python rounds to the nearest even number (this is called "bank rounding")

### ndigits

Examples with `ndigits', the second parameter of the `round()` function

Rounding to one decimal place

```python
result = round(3.14159, 1)
print(result) # Output: 3.1
```

Rounding to three decimal places

```python
result = round(3.14159, 3)
print(result) # Output: 3.142
```

Rounding to zero decimal places is equivalent to rounding
to an integer

```python
result = round(3.14159, 0)
print(result) # Output: 3.0
```

The `round()` function is often used for:

>Simplifying numbers for output.

>Limits on the number of decimal places in calculations.

>Data preparation for further processing.