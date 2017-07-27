---
layout: post
title:  "Working with Files!" - Part 1
date:   2017-07-27 14:39:48 +0100
categories: basic-python
---

All right guys, now that we saw how to deal with the [operative system][opsys] and how to tame for and if cycles, we can push a bit more on the power of Python and deal with Files!

Today we will learn how to read file and play with the `read` option


# Reading files

Differently from C, working with files in Python is straight and painless:
{% highlight python %}
import sys

filename = sys.argv[1]
ifile = open(filename,"r")
#now let's print the lines of the file
lines = ifiles.readlines()
for line in lines:
    print(line)
{% endhighlight %}

In this script we are opening a file, passed with the `sys` command `sys.argv[1]` and we go through it reading each line:
- `ifile=open(filename,"r")`: with `open` we open the file. The most important part here is the `r` which means `read`. So we are opening the `filename` under the option `read`. Other option that can be passed are:
	- `w` : we will use it to `write` new files
	- `a` : `append` is useful to append new lines to an already existing file
	- `wb`: `write binary` rather than writing in human readable format
	- `rb`: `read binary` read a binary file. 
Binary is a necessary hcoice when huge files are created, avoiding memory errors and computational cost
- `lines=ifiles.readlines()`: with the command `.readlines()`, take care of the `()` after the command, this mean *callable*, we will come back later on this topci. `readlines()` returns all the lines of the file. Thus, to read each line and operate on them what do we need? Obviously a for-loop:
- `for line in lines:` : with this for-loop we are reading all the lines given by lines. Thus, we are learning a new powerful method given by the for-loop: given a `list` of things we can go through each element simply by passing this list to a for variable!  


Let's play a bit with the files:

> **Question**: can you create a script which reads [this file][inptfile] and return the total number of lines of it?
>**[Answer][readlines]** If you want to see an answer just click :)  


>**Question**: try to create a script which reads the first 5 lines of [this file][inptfile]

>**[Answer][readfirst]** If you want to see an answer just click :)  


>**Question**: and now try to read the latest 5 lines of [this file][inptfile]

>**[Answer][readlast]** If you want to see an answer just click :)


>**Question**: and now can you create a script which prints out just an interval of lines? For example, I would like a script that can be run as: `python script.py ipt.dat 30 35` where `ipt.dat` is the [inputfile][inptfile] and `30 35` define the interval of lines I want.

>**[Answer][readinterval]** If you want to see an answer just click :)


>**Question**: and finally, can be possible to repeat the previous exercises but printing the lines in reverse order? 

>**[Answer][readintervalreverse]** If you want to see an answer just click :)




[opsys]: module-os.html
[inptfile]: ../../../../assets/2017-07-27/ipt.dat
[readlines]: readlines.html
[readfirst]: read5.html
[readlast]: readlast5.html
[readinterval]:readinterval.html
[readintervalreverse]:readintervalreverse.html