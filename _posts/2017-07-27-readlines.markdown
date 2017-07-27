---
layout: post
title:  "Working with files - Readlines"
date:   2017-07-27 14:39:48 +0100
categories: basic-python
---

# Read the total number of lines of a file


**Answer**
{% highlight python %}
filename = sys.argv[1]
ifile = open(filename,"r")
lines = ifile.readlines()

counter = 0 

for line in lines:
    counter+=1
    
print("Total number of lines %d" % counter)
{% endhighlight %}

If you prefer `counter+=1` can be written as:
`counter = counter +=1`



