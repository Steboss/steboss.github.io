---
layout: post
title:  "Working with files - Read an interval reverse"
date:   2017-07-27 14:39:48 +0100
categories: basic-python
---

# Read in reverse order a given interval of lines


**Answer**
{% highlight python %}
filename = sys.argv[1]
ifile = open(filename,"r")
lines = ifile.readlines()

#now take the input of the interval lines
start = sys.argv[2]
stop  = sys.argv[3]

#check if the start and stop values are within the file 
#range

max_lines = len(lines)

if (start > max_lines):
    print("Please, give a starting point less than %d" % max_lines)
    sys.exit(-1) #this will cause the script to stop
elif stop>max_lines:
    stop = max_lines 
    tot_print = stop - start
    print("I will print only %d lines, since %d is greater than max_lines" % (tot_print,stop))
else:
    continue # if everything is ok continue with the script


for i in range(stop,start,-1)
    print(lines[i],end="")

{% endhighlight %}




