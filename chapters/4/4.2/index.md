# Chapter 4.2 - git

git is a modern, distributed source code versioning system.

[TOC]

## Version control

The need for versioning text has existed for almost as long as writing has existed. There are books with a "2nd revised Edition" for example. Entire encyclopedias are versioned (e.g. Encyclopædia Britannica 1995, Encyclopædia Britannica 1999, etc.).

In software development version control (also known as revision control, source control, or source code management) is a class of systems responsible for managing changes to source code and other related files.

Computers give us the possibility however, to version text much more efficiently.

If you own a full copy of the 2001 revision of Encyclopædia Britannica, you had 32 books on your shelf. If you wanted to use the updated revision of 2002, you'd had another set of 32 books. You could throw the old revision out of course or donate it to someone, but then you wouldn't be able to compare how an article developed between those two versions. Continue this with a few mor revisions and you end up with a whole room full of those books where most of the articles are the same (I guess there weren't that many new facts to write about the [1065 Northern Ireland general election](https://en.wikipedia.org/wiki/1965_Northern_Ireland_general_election)).

So instead having to buy the full 2002 edition, a small book containing just the new and changed articles would have sufficed and would have saved a lot of space.

This would have come with a cost however: If you want to read all about [Klingon sexuality](https://en.wikipedia.org/wiki/Klingon_culture#Sexuality), you'd have to look in the update book for 2005 first, if you don't find the article there, check the books of 2004, 2003, etc. until you either find a book where this article was updated or introduced, or until you reach the very first edition of the Encyclopædia from 1768 where the article was first published.

To make things even more compact, updates could contain not only reprints of full articles, in case there where changes, but could only print the lines which have changed.

This however, would be impossible for a human to read. But computers are great at reading stuff like that and thus that's exactly what a version control system is doing.

## git

A number of revision control systems have been in use over the years. I started my career with CVS (Concurrent Versioning System) which was first published in 1986. In 2000 some of the CVS developers, published SVN (Apache Subversion) with the goal of replacing CVS with something more modern.

In 2005, Linus Torvalds, the creator of Linux, wrote git for managing the source code of Linux.

I will slowly introduce you to the concepts of git and distributed version control in the following chapters.

## Initial setup

First you need to ensure that you have git installed:

```plaintext
nomike@max:~$ git       
Command 'git' not found, but can be installed with:
sudo apt install git
```

Just install git, as you are told if it isn't installed already.

Then you have to configure your name and email address:

```plaintext
nomike@max:~$ git config --global user.name "James Bond"
nomike@max:~$ git config --global user.email "007@mi-6.gv.uk"
```

I could bore you now with examples of how to use git, but I'd rather teach you the core concepts of git while you develop a program. So head on to [Chapter 5 - Dates](../../5/).
