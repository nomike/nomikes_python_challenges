# Chapter 3.0 - The if statement

Imagine you're taking a hike and the trail branches off in two different directions. One leads to a beautiful waterfall, the other to a restaurant.

If you are hungry, then you will go to the restaurant if not ("else") you can go check out that waterfall.

That's a good example of an `if`.

[TOC]

## Anatomy of an `if`

Look at this simple example:

```python
a = int(input("Please enter a number between 0 and 100: "))
if (a > 100) or (a < 0):
    print("The number is not within the correct range.")
else:
    print("Well done!")
print("Thank you for your time!")
```

The program starts by prompting the user to input a number. The input is converted to an integer and stored in variable `a`.

An `if` is used to check whether `a` is within the expected range and the program prints out a message accordingly.

The structure of an `if` is as follows:

```python
if <condition>:
    <then>
else:
    <else>
```

It starts wit the keyword `if` followed by a condition. Any expression which results in a boolean can be a condition. A colon ':' marks the end of the condition, followed by a newline.

The next section is a block of code called the "then"-branch.

Optionally it is followed by the `else` keyword, which again ends with a colon and a new line. Another block of code follows, which is called the "else"-branch.

## Code blocks

Blocks of code consist of one or more lines which ar indented by space of tab characters.

You are free to chose how many space or tab characters and what combinations of those you use to indent code blocks, as long as you are consistent within each block.

This is not OK:

```python

if a > 5:
    print("The number is too big.")
    
     print("Please choose another number.")
```

Even though this is valid code

```python
if it_is_raining:
        if it_is_warm:
         take_an_umbrella()
         put_on_a_summer_jacket()
        else:
              stay_home_and_order_food()
else:
 take_the_sunglasses()
```

it looks much nicer if you format it like this:

```python
if it_is_raining:
    if it_is_warm:
        take_an_umbrella()
        put_on_a_summer_jacket()
    else:
        stay_home_and_order_food()
else:
    take_the_sunglasses()
```

Modern IDEs and editors automatically help you maintain consistent indentation.

***Note:** For reasons of simplicity and consistency, you should avoid using tab characters for indentation. In fact most editors and IDEs automatically insert space characters when you hit the tab key.

## I don't have a "then"

While the "else"-block is optional, sometimes you don't need a "then" block:

```python
if file_exists:
else:
    print("The file does not exist!")
```

This will throw an error however, as you are missing the mandatory "then"-block.

You can use the "pass" command, which does absolutely nothing:

```python
if file_exists:
    pass
else:
    print("The file does not exist!")
```

But in this example it is just better to negate the condition:

```python
if not file_exists:
    print("The file does not exist!")
```

## elif

If you want to test a variable against various colors for example, the can become unreadable quite quickly:

```python
if color=="red":
    pass
else:
    if color=="yellow":
        pass
    else:
        if color=="green":
            pass
        else:
            if color=="blue":
                pass
            else:
                print("Unsupported color: " + color)
```

To simplify code like this, the `elif` keyword was introduced which combines `else` and `if`. The same code might be written like this:

```python
if color=="red":
    pass
elif color=="yellow":
    pass
elif color=="green":
    pass
elif color=="blue":
    pass
else:
    print("Unsupported color: " + color)

```

Now that looks much nicer, doesn't it?

## Conclusion

If you think you are ready, head on to [chapter 3.1](../3.1/) which will explain lists, else go back up and re-read sections or experiment with ifs in an example program.
