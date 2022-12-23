# Chapter 2.2 - Scripts, user input and how to make your life easier

[toc]

## Scripts

Everything we've done in python so far, we did in an interactive python session. While this is perfect to try things out and I use it quite often, it has one big drawback: Once you exit the session, everything is lost. And when you enter a new session, you have to type your whole program again.

To prevent this, you could store your code in a file and tell python to just read the instructions from that file instead of prompting you.

You can use any editor for this, but for the beginning I recommend using `nano` as it's one of the easiest to use

I will assume that you are familiar enough with editors and general shell usage. If you are unsure, please refer back to [chapter 1](../../1/) for details.

## Hello, world

A simple program to start with is the common hello world, which I introduced in the previous chapter:

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

The first print statement was fine, but as can see at the second one, python throws an error. The important bit for now is the last line, which tells us about what went wrong.

Lets see what we can learn from it.

It is a `TypeError`, so it looks that there is something wrong with the type of a variable.
The description gives us more details: It complains about not being able to concatenate an integer to a string.

It looks like the variable `a` is a string and not a number.

This is hardly surprising. The `input` function asks the user to input something. This could be any text and does not necessarily have to be a nnumber. So the data returned by it is a string.

One of the core concepts of the python programming language is to be explicit. If something is not visible in the code, it usually isn't there. Other programming languages sometimes might try to do some guesswork here and assume, that when you have a string containing only numeric characters and want to add the number 2 to it, you want the string to be converted to a an integer first.

As this might lead to a lot of surprises in more complex code, python doesn't do that. If you deal with incompatible data types, it will just throw an error at you.

So if you do want to have that string converted to an integer, you have to tell python to do so.

## Converting variables

Luckily there are built in functions which allow you to convert variables from one type to another:

```python
>>> a = "12"
>>> print(int(a) + 2)
14
```

This prints the result as expected. Other functions for conversion are for example `float()` and `str()`.

## Conclusion

Are you ready for your first real program? Head to the [exercise](exercise/) and we'll find out how good of a teacher I've been so far.
