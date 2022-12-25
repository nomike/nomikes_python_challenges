# Chapter 3.1 - Lists

A collection of similar items is called a list.

[TOC]

## Syntax of lists

```python
colors = ["red", "yellow", "green", "blue"]
```

Lists are defined using square brackets, individual elements are separated by commas.

## Empty lists

To define an empty list, you can just use empty square brackets:

```python
participants = []
```

## Accessing specific elements

You can access a specific element of a list, by referencing the index number of the element:

```python
colors = ["red", "yellow", "green", "blue"]
print(colors[0])    # red
print(colors[3])    # blue
```

List elements are numbered sequentially and the first element starts with index 0.

## Code comments

Python allows you to put comments into your code. For this you have to use the `#` character. Everything behind that character up until the end of the line is then ignored by python. This is helpful for explaining code or for temporarily commenting out code.

```python
filename = input("Which file do you want to delete? ")
# delete(filename)
# commented out to not actually delete files
```

## Strings are lists as well

As mentioned in [chapter 2.1](../../2/2.0/), strings are (almost) like a list of characters. Individual characters could be selected as with any list:5

```python
print("Hello"[1]) # e
```

## Extracting subsets of lists

You can also select a subset of a list by using start and end indices separated by a colon:

```python
print("Hello, world"[0:5]) # Hello
```

If you omit either the beginning or the end index, the beginning or the end of the list are used:

```python
hello = "Hello, world"
print(hello[:4]) # Hell
print(hello[7:]) # World
```

If you use negative indices, counting starts from the end:

```python
hello = "Hello, world"
print(hello[:-3])   # Hello, wo
print(hello[-4:])   # orld
print(hello[-3:-1]) # rl
```

## Length of lists

The built-in function `len()` could be used to determine the length of a list:

```python
colors = ["red", "yellow", "green", "blue"]
print(len(colors))  # 4
```

## Appending items to lists

Lists have a function called `append()` which can be used to append values to them:

```python
colors = ["red", "yellow", "green", "blue"]
print(len(colors))  # 4
colors.append("black")
colors.append("white")
print(len(colors))  # 6
print(colors)       # ['red', 'yellow', 'green', 'blue', 'black', 'white']
```

## Extending lists

Try appending a list to another list:

```python
cities = ["Vienna", "London", "Paris"]
new_cities = ["New York", "New Deli"]
cities.append(new_cities) 
print (cities)  # ['Vienna', 'London', 'Paris', ['New York', 'New Deli']]
```

Now that looks weird.

What happened, is that python just took the value of `new_cities`, which is a list, and appended it as a new element to our list of cities.

What we actually wanted to do is to extend our list of cities with the elements inside the other list. We can just tell python to do so:

```python
cities = ["Vienna", "London", "Paris"]
new_cities = ["New York", "New Deli"]
cities.extend(new_cities) 
print (cities)  # ['Vienna', 'London', 'Paris', 'New York', 'New Deli']
```

Now this looks much better.

## Replacing elements in lists

Just select the element and assign a new value to it.

```python
favorite_reindeer = ["Rudolph", "Donner", "Vixen"]
favorite_reindeer[0] = "Flotilla"
print(favorite_reindeer)    # ['Flotilla', 'Donner', 'Vixen']
```

## Inserting elements

The `insert` function allows you to insert elements in a list. It requires the index at which you want to insert the element and the element itself as parameters:

```python
the_best_programs = ["tron", "ram", "flynn"]
the_best_programs.insert(0, "clue")
print(the_best_programs)    # ['clue', 'tron', 'ram', 'flynn']
```

## Removing elements

The function for removing elements is called `remove`. You have to specify the element you want to remove:

```python
prime_numbers = [2, 3, 5, 7, 9]
prime_numbers.remove(9)
```

## Removing the n-th element

If you want to remove an element based on it's index, you can use the `del` statement:

```python
important_things = ["Basic human rights", "Food", "Wealth", "Sleep"]
del important_things[2]
print(important_things) # ["Basic human rights", "Food", "Sleep"]
```

## Strings are immutable

A string in python can never  be changed. All the operations I've just used, which change something in a list, will fail on strings:

```python
>>> secret_command = "Klahtu barada nikt"
>>> secret_command[3] = "a"
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignment
>>> secret_command.append("o")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'str' object has no attribute 'append'
```

There will be more on strings in a later chapter.

## Exercise

The [exercise](exercise/) will show you a way to get help in python and how to teach yourself more about lists.
