# Chapter 3.0 - The if statement

If-Statements allow you to change your programs behavior based on a condition.

A real life example could be: If it is raining, then take an umbrella with you, otherwise wear a t-shirt.

[TOC]

## Then what?

Look at this simple example:

```python
a = int(input("Please enter a number between 0 and 100: "))
if (a > 100) or (a < 0):
    print("The number is not within the correct range.")
else:
    print("Well done!")
print("Thank you for your time!")
```

The program starts by prompting the user to input a number. The input is then directly converted to an integer and stored in a variable.

An `if` is then used to check whether the integer is within the expected range and the program prints out a message accordingly.

The structure of an `if` is as follows:

```python
if condition:
    <then>
else:
    <else>
```

It starts wit the keyword `if` followed by a condition. This can be any expression which results in a boolean. A colon ':'marks the end of the condition. Followed by a newline.

The next bit is the "then" branch (similar to a tree, when there is a branch off to the side you can opt to either follow it or stay on the current one).

It is followed by the `else` keyword, which again ends with a colon and the "else" branch.

### Indentation

A compiler/interpreter needs to know which lines belong to the "then"-branch (also called a block in programming).

In the C programming language this is achieved with curly braces. A block starts with "{" and ends with "}":

```c
if (a > 100) {
    print("The number is too big!");
} else {
    print("The number is not too big!");
}
```

While most people follow this style of formatting, you could also write the same code like this:

```c
    if (a > 100){      print("The number is too big!");} 
        else {
print("The number is not too big!")}
```

or even like this:

```c
if(a>100){print("The number is too big!");}else{print("The number is not too big!")}
```

This is not readable at all. The more complicated your program gets the more important it is to format your code well and do the indentation correctly.

Python chose a different path.
What people do in other languages out of common sense, is an important syntactical element in python. The interpreter simply knows when a block ends by checking the indentation.

So the same `if` in python looks like this:

```python
if a > 100:
    print("The number is too big!")
else:
    print("The number is not too big!")
```

Due to the indentation, there is no need for those curly braces, so there is less code to write. And those braces very often cause headaches because you can't just figure out where in the code you forgot to put close a block, if the compiler is even nice enough to tell you. Sometimes your program just behaves weirdly.

In python it doesn't matter whether you use space or tab characters for the indentation, or how many of those you use, as long as you are consistent.

This will throw an error:

```python
if number > 10:
    print("The number is bigger than 10")
   print("Multiplied by two this is " + (number * 2) + ".")
```

***Warning:** Be careful not to mix space3s and tab characters. Modern IDEs and most editors however, will automatically convert tabs into spaces and prevent you from doing that mistake.*

## I don't have a "then"

While the "else"-block is optional, sometimes you don't need a "then" block:

```python
if file_exists:
else:
    print("The file does not exist!")
```

This will cause an error, as the python is missing the "then"-block.
There are two ways to fix this.

The "pass" command, which just does nothing:

```python
if file_exists:
    pass
else:
    print("The file does not exist!")
```

Or you can simply negate your condition, which might be the more elegant solution in this case:

```python
if not file_exists:
    print("The file does not exist!")
```
