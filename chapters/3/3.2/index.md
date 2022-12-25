# Chapter 3.1 - Loops

One of the advantage of using computers is, that they are very good in repetitions. You can teach them once how to perform a task, and they can do it countless times.

For this you often want to use loops.

[TOC]

## While loops

```python
number = -1

while not (0<= number <= 100):
    number = int(input("Please enter a number between 0 and 100: "))

print ("You have chosen number " + str(number))
```

Similar to an `if` a while-loop starts with the keyword `while` followed by a condition, a colon, and a code-block.

At first the condition is evaluated and if it's true, the entire code block is executed.
After that, the loop starts from the beginning and checks the condition again.
When the condition evaluates to False, the block is skipped and execution continues afterwards.
