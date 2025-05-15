+++
date = '2024-11-23T18:53:24+03:00'
title = 'Code Compiler'
categories = [ "javascript", "fundamentals" ]
+++

A **compiler** is a program that translates source code written in one programming language into another language — most often into machine code that a computer's processor can execute.

---

## Compilation Process

When we write code in a high-level language like C++, Java, or Rust, it cannot be directly understood by the processor. The compiler performs several stages of transformation:

1. **Lexical analysis** – breaks the code into tokens (words, operators, punctuation).
2. **Syntax analysis** – checks if the structure of the code matches the grammar of the language.
3. **Semantic analysis** – validates the logic: variable declarations, type usage, etc.
4. **Optimization** – improves code efficiency by removing redundancy.
5. **Code generation** – converts the optimized code into machine code.
6. **Linking** – connects compiled files together and binds external libraries.

---

## Benefits of Compilation

-  **Speed** – Compiled code runs faster than interpreted code.
-  **Error Checking** – The compiler checks the entire program for errors before running.
-  **Portability** – One source code can be compiled for different platforms.

---

## Examples of Compiled Languages

- C and C++
- Rust
- Go
- Swift

These languages require a compiler like GCC, Clang, or Rustc to convert the source code into an executable program.

---

## Summary

A compiler performs a deep transformation of code — from human-readable form into optimized, executable instructions. Understanding compilation helps developers write more efficient and portable code.