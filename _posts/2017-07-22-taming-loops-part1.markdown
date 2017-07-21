---
layout: post
title:  "Taming loops! - Part 1"
date:   2017-07-22 14:39:48 +0100
categories: basic-python
---

Welcome back :) Today we will see how to tame `for` loops. I will give you an introduction on what a loop is, what/how/why using loops :) 

# Loops

Loops  are **control flow statement** which allows you to perform multiple operations repeatedly. Both in Python and C the most important loops are : `for` and `if`. The former allows you to cycle through some variables, or values of elements _n_-th time ( and you decide how many _n_). The `if` loop is a control loop. At each iteration this cycle checks whether the variable satisfies some conditions.

# For in action

Now let's play a bit with these loops. Open your text editor and write:
{% highlight python %}
for i in range(1,100):
    print("This is i: %d" % (i))
{% endhighlight %}

Save it as `loops.py`, then go to the prompt and type `pyhton loops.py`. What's the output? Let's analyse the script:
- `for i in range(1,100):` : `for` denotes the beginning of a for-cycle; `i` is an undefined variable, which will go from 1 to 100, as given by the instruction `range(1,100)`. The nomenclature for the range instruction is: `range(start,finish)`. NB: there are `:` at the end of the statement. Remember them, otherwise the script will crash
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

Note that `#` is not read by Python and is interpreted as a comment.

- `print("This is i: %d" % (i))` : this is the instruction to execute at each cycle.

We can make some variations on theme and try different options on with for loops. Open a new file and type
{% highlight python %}
for i in range(0,2000,2):
    print("This is even i %d" % i)
{% endhighlight %}

Save it as `for_even.py` and try to make it run on the prompt. This script will print out only even numbers. Why? That's because we have added a `step` to our range of values: `range(0,2000,2)`. So now we will range from 0 to 2000 with step 2 : 0,2,4,6,8,...100,102,104...1996,1998,2000. Thus, the real nomenclature for range is: `range(start,finish,step)`.


For loops are extremelly powerful and helpfull and without a doubt we will use them a lot in the future.

Obviously we can use a `for` loop in another `for` loop, creating `nested-loops`. Open a new file and call it `timestables.py` and write:
{% highlight python %}
for i in range(1,4):
    for j in range(1,4):
        i_times_j = i*j
        print("%d" % (i_times_j))
    print("\n")
{% endhighlight %}

Here we are doing a multiplication between `i` and `j`. At the first cycle `i=1` and `j=1` thus we will have `1`. Then, at the second cycle `i=1` and `j=2` giving `2`. At the third and last cycle `i=1` and `j=3` so we will have `3` printed out. What's important is to notice that first we are cyclying through all the values of the more nested loop - in this case `j`. Once we have finished with the more nested loop we will go on with the next value in the outer loop. 
Here, once `3` is printed out, in the next step `i=2` and `j=1`. Then , `i=2` and `j=2` and finally `i=2` and `j=3` and so on.
This is really important to keep in mind to prevent from doing to many useless calculations. NB the last values in the `range` instruction. This last values is never reached!

As an example, let's try a three nested loops:
{% highlight python %}
for i in range(1,3):
    for j in range(1,3):
        for k in range(1,3):
            ijk = i*j*k
            print("%d" % (ijk))
    	print("\n")
    print("\n")
print("\n")
{% endhighlight %}
In this case we will have:
- first cycle: `i=1`, `j=1` and `k=1`
- second cycle: `i=1`, `j=1` and `k=2`
- third cycle: `i=1`, `j=2` and `k=1`
- fourth cycle: `i=1`, `j=2` and `k=2`
- fifth cycle: `i=2`, `j=`1` and `k=1`
- sixth cycle: `i=2`, `j=1` and `k=2`
- seventh cycle: `i=2`, `j=2` and `k=1`
- eighth cycle: `i=2`, `j=2` and `k=2`

Finally, note the `print("\n")`. `\n` is a special character and means "newline". When `print` reads `newline` it will print ona new line

Today we have done a lot of things, trust me. So why don't we have a bit of exercise on for loops?

## EXERCISE


>**Question**: can you write a script for a countdown? Starting from 10 print out "10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0"


>**[Answer][countdown]** If you want to see an answer just click :)  



>**Question**: can you write a script that prints out the timestable of 5? In particular, it could be great if the script could print out "5 times 1 equals 5", "5 times 2 equals 10" and so on for each iteration.

>**[Answer][times5]** If you want to see an answer just click :)  



>**Question**: can you write a script that prints out all the timestables as in the Pythagorean tables?

>**[Answer][timestables]** If you want to see an answer just click :)  



>**Question**: Can you write a script which give as output the elements of a 3x3 matrix, whose elements are the multiplication of i ranging from 1 to 4 and j, ranging from 1 to 4? When printing out the results it could be great to see the elements as "1,2,3", so divided by a comma - hard exercise

>**[Answer][matrixnested]** If you want to see an answer just click :)  

Further exercises can be found [here][furtherexercises]


### Little Pro
If you want to see how fast are the loops just time them in this way. Open a new file in the editor and write:
{% highlight python %}
import time
start = time.time()
for i in range(1,100):
    print("This is i:%d" % (i)) 
end = time.time()
print("Time for 100 values loop: %f" % (end - start))
{% endhighlight %}
By modifying the range you can see how much time the loop requests. Usually for this kind of things `for` loops are extremelly fast, taking less than 1microsecond.

[countdown]: countdown.html
[times5]: times5.html
[timestables]: timestables.html
[matrixnested]: matrixnested.html
[furtherexercises]: forloopexercises.html