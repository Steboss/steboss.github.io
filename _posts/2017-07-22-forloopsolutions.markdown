---
layout: post
title:  "Taming loops! - Part 1 - For Solutions"
date:   2017-07-22 14:39:48 +0100
categories: basic-python
---

# Solution for for loop [exercises][forloopexe]

>1) Write a Python program to print out the following pattern:
>*
>**
>***
>****
>*****
>******
>*******
>This script can be useful when you are hackering something, it's your signature

**Answer**

{% highlight python %}
n=7
for i in range(n):
	#i will go throught 0,1,2,3,4,5,6 
	#so you can also give a range without saying where to start
	for j in range(i):
	#this is the key of the exercises
	    print("*",end="")
	    #print will be executed j-th times
	    #end="" states there's no new line 
	    #try to do the same without end=""

	print("")
{% endhighlight %}


>1b) Write a Python program to print out the following pattern:
>*
>**
>***
>****
>*****
>******
>*******
>******
>*****
>****
>***
>**
>*

**Answer**

As before:
{% highlight python %}
n=7
for i in range(n):
	for j in range(i):
	    print("*",end="")

	print("")

for i in range(n,0,-1)
    for j in range(i):
       print("*",end="")
    print("")
{% endhighlight %}


>2) Write a Python program to print out the reverse of the word: "bosibosibosibosi"

**Answer**

Here a new aspect of for cycle: we can go through strings
{% highlight python %}

string = "bosibosibosibosi"
n = len(string)  #len(string) gives the length of the string
for c in range(n-1,-1,-1):
    print(string[c])
{% endhighlight %}

Don't worry if you did not succeed in doing this exercise. Everything will be clearer when we will talk about lists.


>3) Write a Python program to create a 3X3 matrix/array where the element of the _i_-th row and _j_-th column is `i*j`

**Answer**
{% highlight python %}
for i in range(1,4):
    for j in range(1,4):
        elem = i*j
        #print("%d," % elem,end="")
    #print("")
{% endhighlight %}

>4) Try to extend the script in 3) to a 10X10 matrix. In this case try to print out all the matrix rows in this way : `row1: elem1,elem2,elem3,elem4,elem5,elem6,elem7,elem8,elem9,elem10`

**Answer**
{% highlight python %}
for i in range(1,11):
    for j in range(1,11):
        elem = i*j
        print("%d," % elem,end="")
    print("")
{% endhighlight %}

>5) Try to compute the average of the numbers between 1-100 with a for loop.

**Answer**
{% highlight python %}
sum = 0
for i in range(1,101):
    sum = sum + i
    #otherwise: sum+=i
n = 100
average = sum/n
print("Average %.2f" % average)

{% endhighlight %}



