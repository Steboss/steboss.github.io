---
layout: post
title:  "Working with files - Timestables in a file"
date:   2017-07-27 14:39:48 +0100
categories: basic-python
---

# Write times tables form 1 to 10 in a file


**Answer**
{% highlight python %}

ofile = open("timestables.dat","w")

outline = ""
for i in range(1,11):
    for j in range(1,11):
        product = i*j
        outline+="%d times %d equals %d\n " %(i,j,product)
    ofile.write(outline)
    outine=""
{% endhighlight %}




