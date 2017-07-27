---
layout: post
title:  "Working with Files! - Part 2"
date:   2017-07-27 14:39:48 +0100
categories: basic-python
---

Let's start the Part 2 of working with files. In last session we saw how to read files and play with this option. Nowaday we will work with the `write` option.
So let's write Dante's Inferno!


# Writing files

Always differntly form C, writing files in Python is not so complicated:
{% highlight python %}
import sys

filename = sys.argv[1]
ifile = open(filename,"w")
#let's write a timestable:
ifile.write("This is the timestable of 5\n")

for i in range(1,11):
    product = 5*i
    ifile.write("5 times %d equals %d\n" % (%i,%product))

ifile.close()
{% endhighlight %}

As you can see there are a lot of new things:
- `ifile =open(filename,"w")` : as I told you before, the option `w` allows us to write on a file, specificed by `filename`. **Pay attention** : if the file does not exist it will be automatically created, otherwise it will be **overwritten** - so always check before writing a new file
- `ifile.write("This is the timestable of 5\n")` : This statement is exactly the same as `print` statement. We have a string which is written rather than printed out. `ifile.write` start the function `write` on file. In the brackets there will be the line to write. As for `print` the same rules apply here.
-`ifile.close()`: It's a very good practice to close the file once you've written what's necessary.

Now that we know how to read a file and write a file we can mix the two things. In the next script we will read some numbers from two files and we will moltiply them. The files are [factor_1][factor_1] and [factor_2][factor_2], the script will take them as an input from the user and multiply the numbers in factor_1 by all the numbers in factor_2:
{% highlight python %}
import sys

factor_1 = sys.argv[1]
factor_2 = sys.argv[2]
outputfile = sys.argv[3]

ifile1 = open(factor_1,"r")
ifile2 = open(factor_2,"r")
ofile = open("results.dat","w")

read1 = ifile1.readlines()
read2 = ifile2.readlines()

#now cycle through both read
for val1 in read1:
    for val2 in read2:
    	#convert each number into a int
    	elem1 = int(val1)
    	elem2 = int(val2)
        product = elem1*elem2
        ofile.write("%d times %d equals %d\n" %(elem1,elem2,product))

ofile.close()
{% endhighlight %}

Go to the and run this script!
This script represents your first very high achievement in Python world - in my opinion. As you can see we are combining everything. We are first reading all the files and opening a new file. Then we are cycling to each line. Take care that when Python reads a file all the values are considered `string` so we need to convert them (for example: `elem1 = int(val1)` is a conversion of a `string` into an `int`).
Finally, we are printing everything onto a file which is closed in the end.

Now you are ganing a lot of power on your system. You know how to handle folders and directories with the `os` module and how to create and read files. Try these exercises:



> **Question**: Create a file where all the timestable from 1 to 10 are written
>**[Answer][filetimestables]** If you want to see an answer just click :)  


So far so good, now we can deal with this [exercise page][fileexercises] on files! Good luck :)

[factor_1]: ../../../../assets/2017-07-27/factor_1.dat
[factor_2]: ../../../../assets/2017-07-27/factor_2.dat
[filetimestables]: filetimestables.html
[fileexercises]: fileexercises.html