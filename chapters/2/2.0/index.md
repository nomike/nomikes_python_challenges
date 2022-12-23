# Chapter 2.0 - The interactive python interpreter

Already the title of this chapter includes three words, worthy of explanation.

[TOC]

## Machine code

In order to understand what an interpreter is, we first need to understand what machine code (sometimes also called machine language) is.

As I already mentioned, computers only work in binary. The central processing unit (CPU) has wires coming in and out, which can either carry a voltage or not, and these two states represent the numbers 1 and 0.

For a CPU to calculate the sum of the decimal numbers 10 and 32 you need to tell the CPU to store the number 10 in place a, store the number 32 in place b and then tell it to calculate the sum of whatever is currently stored in a and b and store the result in place c.

Depending on what type of CPU you have, there are specific sequences of binary numbers, which tell the CPU to perform these actions.

Early computers had holes which you had to connect with cables to set lines to 1 or 0 and thus program the machine.

<img src=".res/eniac.jpeg" alt="ENIAC - Electronic Numerical Integrator and Computer (photo taken between 1947 and 1955)" width="1340" height="1024" style="height: auto; max-width: 80%" />

Later machines used switches.

But this was cumbersome, error prone and difficult to learn.

## Assembly language

To make things easier, assembly language was introduced throughout the 1940s and 1950s. It allowed to use a more human friendly approach of programming.

The above example of adding 10 and 32 could look like this in assembly:

```asm
mov eax, 10
mov ebx, 32
add eax, ebx
```

It is much easier then connecting wires, but still not easy to do.

If you send these characters to the CPU however, it will not understand it, as it only understands machine code.

So you need a program, which converts that text into machine code, and this is called an assembler.

## High-level programming languages

As time moved on, computers got more powerful and people wanted to perform more complex tasks with them, which was difficult to do in assembly. Assembly is also very close to the hardware (that's why it is called a low-level programming language). The above sample program would run on todays Intel x86 based CPUs, but you would be out of luck on an old Commodore 64 or even a modern smartphone as they use different CPU architectures.

To combat these issues, high-level programming languages where invented, some of which are much more related to a natural language (mostly English).

So in a modern language, the above example is as easy as

```python
10 + 32
```

## Compilers

Code from these high-level languages again needs to be translated into machine code, so that the CPU can use it. One way of doing so is a compiler, which takes the program you have written (the source code) and converts it into machine language. At the end you get a binary file, which can be sent to the CPU and make it do whatever you need.

## Interpreters

Interpreters are another way of executing high-level programming code. Instead of converting your whole program into a big blob of machine code at once, an interpreter takes the first line of your code, converts it to machine code, let's the CPU execute it, takes the next line of your code and repeats that process over and over.

There are pros and cons for both concepts and many programming languages use even more advanced methods, but that's a story for another timer perhaps.

C, the programming language in which unix and linux are written, is usually used with a compiler.
Python is usually interpreted.

However, compilers for python and interpreters for C do exist, but they are not that common (please excuse that I'm greatly simplifying how python works here).

## python

Python was created in the late 1980s with the goal of being a simple, easy to read and easy to learn programming language. Rather than building all of its functionality into its core, Python was designed to be highly extensible via modules. This makes it very flexible and popular. A lot of programs and tools are written in python nowadays.

## A word on python versions

In October 2000 python 2.0 was released and it quickly started to become a success. Minor revisions (2.1, 2.2, ... up until 2.7) followed, but in December 2008 python 3.0 was released.

While python 3.0 (or python3 for short) follows the same principles, it introduced changes to the language which make it incompatible with python2. In 2020 version 2.7 and thus the last one within the 2.x range was declared end-of-life. Most operating systems now no longer ship python2 and default to python3.

However, it might be that the `python` still refers to version 2.7 on your system. If you use Ubuntu, you should be fine however.

To double check this you can use the `--version` parameter:

```plaintext
nomike@max:~$ python --version
Python 3.10.7
```

If it shows a 2.7 version for you, you could try executing python3 directly:

```plaintext
nomike@max:~$ python3 --version
Python 3.10.7
```

In case this doesn't work, you might need to ask a friend or google to figure out how to solve this for your particular setup.

## Interactive

The last word to explain from the headline is "interactive". It means that you can just start the python interpreter and write code, which get's executed whenever you press enter.

```plaintext
Python 3.10.7 (main, Nov 24 2022, 19:45:47) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```

As this chapter was just about explaining terms and giving you a bit of background knowledge, there is no exercise and you should head straight on to [chapter 2.1](../2.1/) where you will have your first interactive python experience, which brings you very close you your first real python program.
