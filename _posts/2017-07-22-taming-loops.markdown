---
layout: post
title:  "Taming loops!"
date:   2017-07-22 14:39:48 +0100
categories: basic-python
---

Welcome back :) Today we will see how to tame `for` and `if` loops. I will give you an introduction on what a loop is, what/how/why using loops :) 

# Loops

Loops  are **control flow statement** which allows you to perform multiple operations repeatedly. Both in Python and C the most important loops are : `for` and `if`. The former allows you to cycle through some variables, or values of elements _n_-th time ( and you decide how many _n_). The `if` loop is a control loop. At each iteration this cycle checks whether the variable satisfies some conditions.

# For and If in action

Now let's play a bit with these loops. Open your text editor and write:
{% highlight python %}
for i in range(1,100):
    print("This is i: %d" % (i))
{% endhighlight %}

Save it as `loops.py`, then go to the prompt and type `pyhton loops.py`. What's the output? Let's analyse the script:
- `for i in range(1,100):` : `for` denotes the beginning of a for-cycle; `i` is an undefined variable, which will go from 1 to 100, as given by the instruction `range(1,100)`. NB: there are `:` at the end of the statement. Remember them, otherwise the script will crash
- `    `: it's not a mistake, this are 4 blank space - or `tab`. For each loops we are creating, Python wants **indentations**. So for example:
{% highlight python %}
for i in range(1,100):
    #four blank spaces
    do something
    for j in range(1,100):
        #further four blank spaces
        do something
        for k in range(1,100):
            #other four blank spaces
            do something
            for w in range(1,100):
                #other four blank spaces
                do something
{% endhighlight %}

- `print("This is i: %d" % (i))` : this is the instruction to execute at each cycle.


For loops are extremelly powerful and helpfull and without a doubt we will use them a lot in the future.


## Little Pro
If you want to see how fast are the loops just time them in this way. Open a new file in the editor and write:
{% highlight python %}
import time
start = time.time()
for i in range(1,100):
    print("This is i:%d" % (i)) 
end = time.time()
print("Time for 100 values loop: %f" % (end - start))
{% endhighlight %}
By modifying the range you can see how much time the loop requests. Usually for this kind of things `for` loops are extremelly fast, taking less than 1$\mu$s