# Chapter 2.2 - Scripts, user input and how to make your life easier

[TOC]

## Scripts

Everything we've done in python so far, we did in an interactive python session. While this is perfect to try out things and I use it quite often, it has one big drawback: Once you exit the session, everything is lost. And when you enter a new session, you have to type your whole program again.

To prevent this, you could store your code in a file and tell python to read the instructions from that file instead of prompting you.

You can use any editor for this, but for the beginning I recommend using `nano`, as it's one of the easiest to use.

I will assume that you are familiar enough with editors and general shell usage. If you are unsure, please refer back to [chapter 1](../../1/) for details.

## Hello, world

A simple program to start with, is the common hello world, which I introduced in the previous chapter:

```python
print('hello, world')
```

Create a file named `hello.py` and put the above print-statement in it.

Once your file is saved and you are back at the shell, you could use python to run your script:

```plaintext
$ python hello.py
hello, world
```

## Concatenating strings

You can concatenate a string to another one by using the `+` operator:

```python
>>> "Hello, " + "world"
'Hello, world'
```

## Getting user input

The function `input()` requests the user to enter a value.

```python
>>> a = input("Please enter a number: ")
Please enter a number: 12
>>> print(a)
12
>>> print(a + 2)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

The first print statement was fine, but as you can see at the second one, python throws an error. The important bit for now is the last line, which tells us about what went wrong.

Lets see what we can learn from it.

It is a `TypeError`, so it looks that there is something wrong with the type of a variable.
The description gives us more details: It complains about not being able to concatenate an integer to a string.

What we have just discovered is, that apart from being dynamically typed, python is also strongly typed.

## Strong typing

Python is a strongly typed language. That means, that variables do have a type and that that type matters when performing operations on them.

As you have seen in the example above, python complained that it can't concatenate an integer to a string.

```python
>>> print(a + 2)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

Some programming languages are weakly typed, which means that the compiler/interpreter might just convert the `3` to a string `"3"` and append it to the other string. This happens implicitly behind the scenes and you might not be aware of if, which could cause all kinds of issues and bugs.

Python, on the other hand, follows the philosophy that things should be explicit: If you want something to happen, you have to write it.

Thus the code could be written as:

```python
>>> print(a + str(2))
'122'
```

However, it is more likely you actually wanted to write this:

```python
>>> print(int(a) + 2)
14
```

## Converting variables

There are built in functions which allow you to convert variables from one type to another:

```python
>>> a = "12"
>>> print(int(a) + 2)
14
```

This prints the result as expected. Other functions for conversion are for example `float()` and `str()`.

## Conclusion

Are you ready for your first real program? Head to the [exercise](exercise/) and we'll find out how good of a teacher I've been so far.
