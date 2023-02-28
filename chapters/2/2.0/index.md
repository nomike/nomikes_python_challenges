# Chapter 2.0 - The interactive python interpreter

The title of this chapter already includes three words worthy of explanation.
But before we dive into that, I want to tell you a little bit about the history of computer programming languages.

[TOC]

## Some backstory first

### Machine code and how a CPU works

In order to understand what an interpreter is, we first need to understand how a CPU works and what machine code (sometimes also called machine language) is.

A very basic CPU has pins (also called lines) which are connected to the rest of the system. There are lines for inputting data, lines for outputting data and lines for inputting commands.

A CPU also contains a few tiny data storage places where it can temporarily store simple values. These are called registers.

If you want the CPU to add the numbers 10 and 32, you would need to perform a few steps:

1. Set the data-input pins to the binary representation of the number 10 and send the "store data from input to register a" instruction.
2. Set the data-input pins to the binary representation of the number 32 and send the "store data from input to register b" instruction.
3. Send the "calculate the sum of register a and register b and store the result in register a" instruction to the CPU

You can then continue with other instructions and further manipulate that data.

Early computers had contact-panels where you had to run jumper wires between points to input data and instructions. Output was displayed with lamps who where either on or off.

<img src=".res/eniac.jpeg" alt="ENIAC - Electronic Numerical Integrator and Computer (photo taken between 1947 and 1955)" width="1340" height="1024" style="height: auto; max-width: 80%" />

Later machines simplified things and used switches.
But this was still cumbersome, error prone and difficult to learn.

### Assembly language

To make things easier, assembly language was introduced throughout the 1940s and 1950s. It allowed to use a more human friendly approach to programming.

The above example of adding 10 and 32 could look like this in assembly:

```asm
mov eax, 10
mov ebx, 32
add eax, ebx
```

It is much more convenient then connecting wires, but still not easy to do. You need to understand a lot about the internal workings of your CPU and the rest of your computers components an how they interact with each other. Simple tasks could require a lot of instructions to be executed by the CPU.

If you send these code to the CPU as characters however, it will not understand it, as it only understands the 1s and 0s ot machine code which we talked about earlier.

You need a program, which converts that text into machine code, and this is called an assembler.

### High-level programming languages

As time moved on, computers got more powerful and people wanted to perform more complex tasks with them, which was difficult to do in assembly. Assembly is also very close to the hardware (that's why it is also called a low-level programming language). The above sample program would run on todays Intel x86 based CPUs, but you would be out of luck on an old Commodore 64 or even a modern smartphone as those use different CPU architectures where the instructions are completely different.

To solve these issues, high-level programming languages have been invented.

In a modern language, the above example is as easy as

```python
10 + 32
```

### Compilers

Code from these high-level languages again needs to be translated into machine code, so that the CPU can use it. One way of doing so is by using a compiler.

A compiler takes the program you wrote (the source code) and converts it into machine language. When it's done you get a binary file, which can be sent to the CPU to make it do whatever you need.

### Interpreters

Another way of executing high-level programming code are interpreters.
Instead of converting your whole program into a big blob of machine code at once, an interpreter takes one line of your code, converts it to machine code, let's the CPU execute it, takes the next line of your code and repeats that process over and over.

There are pros and cons for both concepts and many programming languages use even more advanced methods, but that's a story for another timer perhaps.

All you need to know for now, is that python typically is interpreted.

## Python

Python was created in the late 1980s with the goal of being a simple, easy to read and easy to learn programming language.

The syntax is easy to understand and learn. It is easy to extend the language and thus python is very versatile and powerful. Despite that it managed to stay very simple.

This makes it very popular and a lot of programs and tools are written in python nowadays.

### A word on python versions

For a long time python version 2.x was used but it was slowly replaced by python 3.
While both versions belong to the same language family, there are certain incompatible differences between them.

As python 2 was declared end of life years ago, everyone should have switched to python 3 already. Thus this course will only cover python 3.

If you're running an older version of your operating system, you still might have python 2 installed on your computer.

You can check this with the `--version` parameter of the python command:

```plaintext
nomike@max:~$ python --version
Python 3.10.7
```

If it shows a 2.7 version for you, you could try executing python3 directly:

```plaintext
nomike@max:~$ python3 --version
Python 3.10.7
```

If `python3` gives you a "command not found" error message or something similar, you might want to consider updating your operating system. Or ask google or a friend for assistance as it will be hard following the remainder of this course if you are using python 2.

## Interactive

I almost forgot that there is one last word left from the headline which needs explanation: "interactive".
It means that if you just start the python interpreter, you will get a prompt where you can directly input python code which gets executed right away:

```plaintext
Python 3.10.7 (main, Nov 24 2022, 19:45:47) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

***Note:** You already used in interactive session for an interpreted programming language. Your shell. `bash`, the shell most commonly used in linux distributions nowadays, is an interpreter as well, just like python. It has a different syntax though and other major differences.*

This is a great way to quickly test code and you will have the chance to try it out in the next [chapter](../2.1/) where you will have your first interactive python experience, which brings you very close you your first real python program.
