# Chapter 2.2 - Scripts, user input and how to make your life easier

[toc]

## Scripts

Everything we've done in python so far, we did in an interactive python session. It's perfect to try things out and I use it quite often, but it has one big drawback: Once you exit the session, everything is lost and when you enter a new session, you have to type in everything again.

To prevent this, you could store your code in a file and tell python to just read the python code from that file instead of prompting you.

You can use any editor for this, but for the beginning I recommend using `nano`.

I will assume that you are familiar enough with editors and general shell usage. If you are unsure, please refer back to [chapter 1](../../1/) for details.

## Hello, world

A simple program to start with is the common hello world, which I introduced in the previous chapter:

```python
print('hello, world')
```

Create a file named `hello.py` now and put the above print-statement in it.

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
>>> print(a+2)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```

As you could see python throws an error. The important bit is the last line, which tells us about what went wrong.

It is a `TypeError`, so it means that there is something wrong with the type of a variable. The description gives us more details. It complains about not being able to concatenate an integer to a string.

So obviously, the variable `a` is a string and not a number.

But this is hardly surprising, as the user could have entered anything when prompted for input, even text.

One of the core concepts of especially the python programming language is to be explicit. If something is not visible in the code, it usually doesn't happen. Python couldn't know if the "12" you entered is meant to be the literal text "12" or the integer 12.

So you have to tell python, that in this case you want the "12" to be converted to an integer.

## Converting variables

There are functions which allow you to convert variables from one type to another:

```python
>>> a = "12"
>>> print(int(a) + 2)
14
```

This prints the result as expected. Other functions for conversion are for example `float()` and `str()`.

Are you ready for your first real program? Head to the [exercise](exercise/) to find out how well I explained the basic concepts of python programming to you so far.