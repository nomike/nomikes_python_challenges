[TOC]

# Navigate through folders

The exercise in this chapter is quite simple. Open a shell and create a folder called "c1".
Move into that folder and play around in it.

Create files, folders, folders within those folders and files within them.

Try to move around, delete files, delete folders, etc..

Try deleting a file with "rmdir", try deleting a folder with "rm" and see what happens when you try to delete a folder which has a file or another folder in it.

# Built-in help

Almost all unix tools have a built in help which can be accessed with the `--help` parameter:

```plaintext
nomike@max:~/coding/nomikes_python_challenges$ pwd --help
pwd: pwd [-LP]
    Print the name of the current working directory.
    
    Options:
      -L        print the value of $PWD if it names the current working
                directory
      -P        print the physical directory, without any symbolic links
    
    By default, `pwd' behaves as if `-L' were specified.
    
    Exit Status:
    Returns 0 unless an invalid option is given or the current directory
    cannot be read.
```

This usually gives you a brief overview of what the command does, what parameters and options it supports and sometimes has examples for basic tasks you can perform with it.

***Hint:** The help screen could be quite large and overwhelming. You don't need to understand everything, just lookup what you want to know.*

# Recursive delete

You can delete a folder with all of it´s contents. This is called *recursive delete*.
The `rm` command supports a parameter for recursive deletion.

Try to use the built in help of the "rmdir" and "rm" commands to figure out which of those could be used to recursively delete a directory and what options you need to specify.

***WARNING:** When recursively deleting a folder, you can do a lot of damage if you delete a folder which contains important system files or your precious vacation photos. That's why you should be careful with what you do. Don't use superuser privileges (`sudo`) unless absolutely necessary and be sure to regularly backup your important files!*

# Delete an empty directory with `rm`

Could you delete an empty directory with `rm`?

# More options for `rm`

What do the options `-f`, `-i`, and `-I` do? Try them out!

# Cleanup

When you're done with this exercise, cleanup by deleting the `c1` folder with all of it's content.

You can now progress to [Chapter 1.1](../../1.1/).