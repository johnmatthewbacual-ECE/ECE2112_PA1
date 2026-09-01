# ECE 2112 - Experiment 1: Introduction to Python Programming

**Name:** Bacual, John Matthew P.

**Section:** 2ECE-A

**Date Submitted:** August 31, 2026

The content of this repository contains *Programming Assignment 1* for **ECE 2112: Advanced Computer Programming and Algorithms for S.Y. 2026–2027**. This project covers three Python programming problems under Experiment 1: Introduction to Python Programming.

## Objective

The objective of this experiment is to develop a basic understanding of Python programming by applying fundamental functions, string operations, string manipulation, and sequence unpacking.

Specifically, the experiment aims to:

1. Use basic Python functions, operators, and string operations.
2. Manipulate strings using indexing, slicing, and built-in string methods.
3. Apply sequence unpacking to manipulate the elements of a list.
4. Construct simple Python functions that return a specified result.

## Detailed Discussion of the Experiment

### A. Word Rotation Problem

The first problem focuses on manipulating a string using **indexing and slicing**. The objective is to create a function named `rotate_word()` that moves the first character of a given string to the end while keeping the remaining characters in their original order.

The function first obtains the first character using `text[0]` and then obtains the remaining characters using `text[1:]`. These two parts are then combined using string concatenation, with the remaining characters placed before the first character.

```python
def rotate_word(text):
    first = text[0]
    rest = text[1:]
    return rest + first
```

The function was tested using the required examples from the experiment, with an additional test using `"Logic"` to verify that the capitalization of the first character is preserved.

**Results:**

```text
rotate_word("python") → "ythonp"
rotate_word("Logic")  → "ogicL"
rotate_word("Code")   → "odeC"
rotate_word("A")      → "A"
```

The results show that the function successfully moves the first character to the end of the string. For the single-character input `"A"`, the result remains `"A"` because there are no other characters to rearrange. The executed outputs can also be seen in the submitted file.

---

### B. Username Builder Problem

The second problem involves processing two strings representing a first name and a last name to create a formatted username. The required function, `make_username()`, converts all letters to lowercase, removes spaces from both names, and joins the processed names using a period.

The solution uses the built-in `.lower()` method to convert the letters to lowercase and `.replace(" ", "")` to remove spaces. String concatenation is then used to combine the first name, a period, and the last name.

```python
def make_username(first_name, last_name):
    first_name = first_name.lower()
    first_name = first_name.replace(" ", "")
    last_name = last_name.lower()
    last_name = last_name.replace(" ", "")
    return first_name + "." + last_name
```

The function was tested using the examples provided in the experiment as well as an additional test case using the student's name.

**Results:**

```text
make_username("Ada", "Lovelace")
→ "ada.lovelace"

make_username("Alan", "Turing")
→ "alan.turing"

make_username("Ana Maria", "De Leon")
→ "anamaria.deleon"

make_username("John Matthew", "Bacual")
→ "johnmatthew.bacual"
```

The results demonstrate that the function correctly converts uppercase letters to lowercase and removes spaces from names such as `"Ana Maria"` and `"De Leon"`. The processed names are successfully combined using a period to form the required username format. The executed test outputs are present in the submitted notebook.

---

### C. Bookend Swap Problem

The third problem focuses on **list manipulation and extended sequence unpacking**. The objective is to create a function named `swap_bookends()` that exchanges the first and last elements of a list while preserving the order of all elements in between.

The required extended sequence unpacking technique is used to separate the list into three parts: `first`, `middle`, and `last`.

```python
def swap_bookends(items):
    first, *middle, last = items
    return [last] + middle + [first]
```

In the line `first, *middle, last = items`, the first element is assigned to `first`, the last element is assigned to `last`, and all elements between them are collected into `middle`. The function then creates a new list by placing `last` at the beginning, keeping `middle` in its original order, and placing `first` at the end.

**Results:**

```text
swap_bookends([1, 2, 3, 4, 5, 6])
→ [6, 2, 3, 4, 5, 1]

swap_bookends(["red", "green", "blue"])
→ ["blue", "green", "red"]

swap_bookends([8, 3])
→ [3, 8]
```

The results confirm that the first and last elements are successfully exchanged while the middle elements remain in their original order. The function also returns a new list rather than modifying the original input list. The executed test results are shown in the submitted Jupyter Notebook.

---

**Thank you for reading!**

To see the main python program for Programming Assignment 1, click this link https://github.com/johnmatthewbacual-ECE/ECE2112_PA1/blob/d5a9773634174aa95ab44c32cf2c6ca8a83a75ec/Bacual_2ECE-A_PA1.ipynb and download. Open on Jupyter Notebook, then run all cells.

README file Version History:
**September 1, 2025** - README output uploaded.

