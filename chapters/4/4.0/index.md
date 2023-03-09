# Chapter 4.0 - ipython3

`ipython3` is a replacement interactive python shell which is more convenient than the standard one.

[TOC]

## Package management

All modern linux distributions use a package management system.

A package management system organizes software in packages. If you want to install a program, the preferred way is to install it using the package manager.

The open source and free software nature of the GNU/Linux ecosystem allows programmers to re-use code. For example: If you want to write an application which allows the user to compile a list of MP3 files and burn them to a CD so you can play it in your old car stereo, you can use an existing tool to convert your MP3 files into a format suitable for audio CDs. You can use another tool to manage your CD burner and actually burn the CD.

The package manager also takes care of these dependencies and installs the audio conversion tool and the CD burner management tool before it install your Audi-CD mastering software.

The package management system used in Ubuntu is called apt and it is available using the `apt` command line tool.

With `apt search waldo` you could search for all packages containing "waldo" in their name.

***Note:** Ubuntu also uses a separate system for managing software called snap. I will show it to you in the next chapter.*

## Installing ipython3

You can simply install ipython3 with apt:

```plaintext
$ sudo apt install ipython3
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  ipython3
0 upgraded, 1 newly installed, 0 to remove and 29 not upgraded.
Need to get 5.238 B of archives.
After this operation, 44,0 kB of additional disk space will be used.
Get:1 http://at.archive.ubuntu.com/ubuntu kinetic/universe amd64 ipython3 all 7.31.1-1 [5.238 B]
Fetched 5.238 B in 0s (42,6 kB/s)
debconf: unable to initialize frontend: Dialog
debconf: (Dialog frontend requires a screen at least 13 lines tall and 31 columns wide.)
debconf: falling back to frontend: Readline
Selecting previously unselected package ipython3.
(Reading database ... 675495 files and directories currently installed.)
Preparing to unpack .../ipython3_7.31.1-1_all.deb ...
Unpacking ipython3 (7.31.1-1) ...
Setting up ipython3 (7.31.1-1) ...
Processing triggers for man-db (2.10.2-2) ...
```

Note that on your system the output might look different. apt might need to install some additional packages and might ask you for consent doing so.

## ipython3

As ipython3 is now installed, you can start an interactive session:

```plaintext
ipython3
Python 3.10.7 (main, Nov 24 2022, 19:45:47) [GCC 12.2.0]
Type 'copyright', 'credits' or 'license' for more information
IPython 7.31.1 -- An enhanced Interactive Python. Type '?' for help.

In [1]:
```

It's not that much different than plain python3. The prompt looks different, buy you can put in the same commands. It features syntax highlighting and tab-completion though, which make coding generally more pleasant.

If you execute a program though, I still recommend using plain python3 (`python3 hello.py` for example).

### Tab-completion

Tab-completion is an invaluable feature present in most shells and IDEs. You type the beginning os something, press the tab key (the one left of "Q" on german oder english keyboards; the one directly above caps-lock; the one furthest left in the upmost row containing letter keys) and the tool tries to completes your input, if there is only one, or gives you a list of options if there is multiple.

So typing "pr" and then hitting tab presents you with the options `print() property %precision %prun %%prun`. You can either continue typing until there is only one matching option left and hit the tab key again (type "i" and hit tab, it will complete to "print"), or repeatedly hit the tab key to highlight the option you want and then press enter to select it. ctrl-c get's you out of tab completion.

***Note:** Tab completion also works in the shell. In bash however, if there are multiple matching options, it completes as far as they are equal and then you have to continue typing. But go ahead and try it out. You can type "cd /" for example and hit the tab key.*

For the ultimate in convenience during programming, look into chapter [4.1 - Visual Studio Code](../4.1/).
