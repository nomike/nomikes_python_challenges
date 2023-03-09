# Chapter 4.1 - Visual Studio Code

A new IDE has emerged over the last couple of years and it turned out to be very decent. Visual Studio code (vscode) is free open source software and is being developed by Microsoft.
It's available for Windows, Linux and macos.

[TOC]

## Installing vscode in Windows Subsystem for Linux

If you are using WSL, it is recommended to install vscode directly in Windows. The preferred way for that is using the Microsoft Store. If you can't use this, you can also download an installation package from [https://code.visualstudio.com/].

In Visual Studio code you might want to install an extension for WSL. To find the extension manager, look at the icons on the left. One looks like four squares being put together. If you hover these icons with your mouse cursor, a tool tip will appear, telling you what it is.

In the extensions manager, search for "WSL" and install the extension published by Microsoft.

***Note:** Very often the list of extensions you get is quite large. Look at the number of downloads for each package. WSL is quite common. So there is an extension with 17.4 million installs and there are others with 35.000 installs. This usually makes it obvious which one to try first.*

## Installing vscode in Ubuntu

In ubuntu you can use package management to install vscode, which makes things easier. However, vscode is not provided via apt. For that snap, the second big software management tool, is used.

Installing software with snap however, is as simple as with apt:

```plaintext
nomike@max:~$ sudo snap install code
error: This revision of snap "code" was published using classic confinement and thus may perform
       arbitrary system changes outside of the security sandbox that snaps are usually confined to,
       which may put your system at risk.

       If you understand and want to proceed repeat the command including --classic.
```

For the moment, just trust me on this, that this is safe and you can just use the `--classic` parameter as advised to install vscode:

```plaintext
nomike@max:~$ sudo snap install vscode --classic
vscode 1.76.0 from Microsoft installed
```

### The python extension

In vscode, you should install the python extension. For information on how to do that refer to the [section about installing vscode in Windows](#installing-vscode-in-windows-subsystem-for-linux) earlier in this chapter.

### A few helpful tips to get you started

When you open vscode you will see a welcome page. I highly recommend reading some of the walkthroughs.

I also like vscode as a general purpose text editor, e.g. for writing notes. The one killer feature IMHO is, that it doesn't ask questions about unsaved files when you close it. It just closes. And next time you start it, all your unsaved files are still there, unsaved as they where before.

There is no specific exercise in this chapter. The exercise is reading through some of those walkthroughs (read as many as you like, but you don't have to read all of them or do them from beginning to end).

Another great resource BTW is to look at the extensions manager. When you search for an extension, you often get a introductory page which gives you an overview of the extension but also shows you some usage examples and general tips and tricks. It's always worth a look.

Once you're done with that, you can head over to [Chapter 4.2 - git](../4.2) where you will learn the merits of a version control system.
