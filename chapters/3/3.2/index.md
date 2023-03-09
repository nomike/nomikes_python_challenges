# Chapter 3.1 - Loops

One of the advantages of using computers is, that they are very good at repeating things. You can teach them once how to perform a task, and they can do it countless times.

For this you often want to use loops.

[TOC]

## While-loops

```python
number = -1 # initialized to -1 so that the while-condition evaluates to True and the user is asked at least once to enter a number

while not (0 <= number <= 100):
    number = int(input("Please enter a number between 0 and 100: "))

print ("You have chosen number " + str(number))
```

Similar to an `if` a while-loop starts with the keyword `while` followed by a condition, a colon, and a code-block.

At first the condition is evaluated and if it's true, the entire code block is executed.
After that, the loop starts from the beginning and checks the condition again.
If the condition evaluates to False, then the block is skipped and execution continues after the loop.

## Endless loops

If you write a loop where the condition never get's false, you got an endless loop. This means that your program will run forever and will never stop.

```python
i = 0
while i < 10:
    i = i - 1
```

If you run this code, you need to press ctrl-c to interrupt the program.

## do-while-loops

Sometimes you want to have a loop which runs at least once.
Some other programming languages use do-while-loops for this. In python, you just create an endless loop and break out of it once a certain condition is met. For this you can use the `break` keyword.

## Break

You can intentionally create an endless loop by using `True` as the condition. The loop will thus run at last once, and you can break out of it, if you want to end the loop.
The example from above, where the user needs to enter a value between 0 and 100, could be written like this:

```python
while True:
    number = int(input("Please enter a number between 0 and 100: "))
    if 0 <= number <= 100:
        break
```

The condition moved down to the `if` and it does no longer need to be negated. `number` doesn't have to be initialized with the arbitrarily chosen `-1` value.

## Continue

Sometimes you want to just stop the execution of the remainder of the loop-block and continue with the next iteration:

```python
# record license plates of all red cars
license_plates = []
while True:
    car = get_next_car()
    if not car.color == "red":
        continue
    license_plates.append(car.license_plate)
```

## For-each-loops

While-loops are great if you don't know how many items you want to loop over. If have a finit list of items however, you might want to use a for-each-loop instead:

```python
colors = ["red", "yellow", "green", "blue"]

for color in colors:
    print(color)
```

This program executes the loop-block for each element of the list `colors`. It assigns the current element to the variable `color` each time before entering the loop-block.

## The `range` function

The range function produces a sequence of numbers.

```python
for i in range(10):
    print(i)
```

prints the numbers from 0 to 9 to the terminal.
You can also specify the start number and the interval.

```python
range(3, 5)      # [3, 4]
range(0, 10, 2)  # [0, 2, 4, 6, 8]
range(10, 0, -1) # [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```

## For-loops with a predefined number of runs

The `range` function comes in handy when you want a loop to be executed a fixed number of times:

```python
password = "REINDEER FLOTILLA"
password_ok = False
for i in range(3):
    password_input = input("Enter password: ")
    if password == password_input:
        password_ok = True
        print("Welcome back Flynn.")
        break
    print("Wrong password. Please try again.")

if not password_ok:
    print("Illegal access. This will be reported to the master control program")
```

## Exercise

With all the stuff you just learned about loops, now is your chance to put your knowledge to the test in this chapter's [exercise](exercise/).
