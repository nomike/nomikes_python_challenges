# Chapter 1.1 - Hidden files, directory separators, the home directory

In this chapter, you will learn about how to hide a file or directory and what the home directory is.

[TOC]

## Hiding files and directories

Let's look at the content of a directory I've just created:

```plaintext
nomike@max:/tmp/example$ ls -l
total 0
-rw-rw-r-- 1 nomike nomike 0 Dez 12 01:27 foo.txt
```

We have learned previously that we could create empty files with the `touch` command:

```plaintext
nomike@max:/tmp/example$ touch bar.txt
```

Let's look at the directory again:

```plaintext
nomike@max:/tmp/example$ ls -l
total 0
-rw-rw-r-- 1 nomike nomike 0 Dez 12 01:28 bar.txt
-rw-rw-r-- 1 nomike nomike 0 Dez 12 01:27 foo.txt
```

Let's create another file now and list our directory:

```plaintext
nomike@max:/tmp/example$ touch .rugby
nomike@max:/tmp/example$ ls -l
total 0
-rw-rw-r-- 1 nomike nomike 0 Dez 12 01:28 bar.txt
-rw-rw-r-- 1 nomike nomike 0 Dez 12 01:27 foo.txt
```

The file is not shown in our directory listing. We have just created a hidden file. Files are hidden, if their name starts with a ".".

Directories could be hidden as well:

```plaintext
nomike@max:/tmp/example$ mkdir .baz
nomike@max:/tmp/example$ ls -l
total 0
-rw-rw-r-- 1 nomike nomike 0 Dez 12 01:28 bar.txt
-rw-rw-r-- 1 nomike nomike 0 Dez 12 01:27 foo.txt
```

As they are only hidden, you could still interact with hidden files and directories:

```plaintext
nomike@max:/tmp/example$ cd .baz/
nomike@max:/tmp/example/.baz$ ls -l
total 0
nomike@max:/tmp/example/.baz$ cd ..
```

## Showing hidden files and directories

The `ls` command has an option for showing hidden files called  `-A`:

```plaintext
nomike@max:/tmp/example$ ls -l -A
total 4
-rw-rw-r-- 1 nomike nomike    0 Dez 12 01:28 bar.txt
drwxrwxr-x 2 nomike nomike 4096 Dez 12 01:34 .baz
-rw-rw-r-- 1 nomike nomike    0 Dez 12 01:27 foo.txt
-rw-rw-r-- 1 nomike nomike    0 Dez 12 01:30 .rugby
```

As you can see, our hidden file and hidden directory now show up.

There is another option which shows us a little more `-a`:

```plaintext
nomike@max:/tmp/example$ ls -l -a
total 24
drwxrwxr-x  3 nomike nomike  4096 Dez 12 01:34 .
drwxrwxrwt 36 root   root   16384 Dez 12 01:26 ..
-rw-rw-r--  1 nomike nomike     0 Dez 12 01:28 bar.txt
drwxrwxr-x  2 nomike nomike  4096 Dez 12 01:34 .baz
-rw-rw-r--  1 nomike nomike     0 Dez 12 01:27 foo.txt
-rw-rw-r--  1 nomike nomike     0 Dez 12 01:30 .rugby
```

In the previous chapter, you've learned that (almost) all directories contain the special items `.` and `..` which refer to the current and to the parent directory. As both of these start with a ".", these are hidden by default as well, and the `-a` option needs to be used to show them.

## Directory separators

In the examples of this course, you have seen directories nested into other directories. To separate directories and files from each other, the forward-slash character (`/`) is used.

For example `foo/bar/baz.txt` refers to a directory "foo" which contains a nested directory (also called a subdirectory) "bar" which contains the file "baz.txt".

## Paths

If you specify directories and possibly a filename, separated by `/`s, which show you where you can find the item, this is called a "path".

### Relative paths

A relative path, tells you, how to get to a certain location, from where you are right now. Relative paths must not start with a `/` character.

Simple paths could be:

```plaintext
Documents/tax-reports/2022.txt
document_root/index.html
Music
```

A path could also contain hidden items. 

```plaintext
.state-secrets/roswell.txt
nomike/.hidden/desires.txt
../readme.txt
./foo.txt
../../
subfolder/././././././../foo.txt
```
As you can see, the special directories `.` and `..` can be used in paths as well.

## The root directory

As you have learned, unix organizes files within directories and you can traverse this hierarchy with the `cd` command. But where does this all start?

At the root directory.

The root directory could be found at the path `/`. All other files and directories are nested within the root directory.

## Absolute paths

If a path starts with a `/` character, it is an absolute path, as it tells you how to find a certain item when you start looking from the root directory.

Some examples for absolute paths

```plaintext
/
/home/nomike/Documents/tax_form2021.txt
/usr/bin/ls
/usr/bin/mkdir
/usr/bin/rm
/etc/users
```
## The home directory

Every user has a home directory. This is typically a directory named after the username and is located in `/home`. My home directory is thus `/home/nomike`.

When you login to a computer or open a terminal emulator, you're current working directory is typically set to your home directory.

As it usually is the directory you use the most, there are two short cuts here:

First of all, if you type `cd` without specifying a directory, it changes to your home directory:

```plaintext
nomike@max:/tmp/example$ cd
nomike@max:~$ pwd
/home/nomike
nomike@max:~$ 
```

And secondly, your home directory is abbreviated as `~`. A `cd ~` also sends you home and you can use it within paths as well. So if your username is `nomike`, the path `/home/nomike/Pictures/portrait.txt` is equal to `~/Pictures/portrait.txt`.

