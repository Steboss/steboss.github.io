---
layout: post
title:  "Hello World, I'm writing Python"
date:   2017-07-21 14:39:48 +0100
categories: basic-python
---

Here we are! Ready to conquer the world by writing the most brilliant, hyper fast and amazing script in Python.
So let's start from the very very basics.
I know, it may be pretty boring all these basics things, but just give a quick read since you will have always to deal with basics!

# Hello World and Variables

Here you have to decide which text editor you like most: on Windows there's _notepad_, but you can also use _nano_, _atom_, _sublime_... there's a world full of text editor suitable for programming.
I prefer _atom_ and _sublime_, so I'll show you everything based on these editors.
Once, you have chosen the text editor type this code:
{% highlight python %}
print("Hello World, I am finally writing Python")
{% endhighlight %}
Save the script as ```helloworld.py```.


Now go to the command prompt (here we need to show a picture or specifiy all the paths)
and type
{% highlight python %}
python helloworld.py
{% endhighlight %}

The Python interpreter ```python``` will read the script and follow the instructions. On the screen will appear: ```Hello World, I am finally writing Python```

What did we do? Let me introduce the three elements we've used:

- ```print``` print is command, or a function. Giving a string as an input it will print out ( on the "standard output") that string
- ```Hello World, I am finally writing Python```: This is the string given as an input to ```print```
- ``` python("Hello World, I am finally writing Python")```: this is the complete form of the instruction we are giving to the Python interpreter to be executed. Python will read the script from the top till the bottom.

Now, what it's useful is the possibility of associating a value to a variable. A variable is like a container and it can be filled ith everything we want (strings, characters, numbers, floating precision numbers, dictionaries...).
Let's see what's going on if we adopt variables for printing:
{% highlight python %}
a = "Hello"
b = "World"
c = "I am writing in Python"
d = "Am I cool, isn't it?"

print("%s %s %s %s" % (a,b,c,d))
{% endhighlight %}


After saving the script as `hellovariables.py`, we execute it in the prompt:
Give the output

In this script we have coupled `print` with four variables `a`,`b`,`c` and `d`. For each variable we want to print we need to tell ```print``` what `type` is that variable. So we have:
- for **strings** : `%s`, as we have done before

- for **integers** : `%d`, e.g. : 

{% highlight python %}
print("%d" % (10))
print("%d" % (234556)))
print("%d" % (1241))
{% endhighlight %}

- for **floating** : `%f`, e.g.:

{% highlight python %}
print("%f" % (1.23456778))
{% endhighlight %}

otherwise if we want a specific number of figures

{% highlight python %}
print("%.4f" % (1.2345))
print("%.8f" % (1.23456789))
{% endhighlight %}


>**Question**  what if we type:
{% highlight python %}
print("%.4f" %(1.23))
print("%.8f" % (1.2))
{% endhighlight %}
>So we give less figures than what expected by print?

>**Question** what if we don't know the type of the variable?
**Answer** If we don't know the type of the variables, the Python interpreter is so clever that it can retrieve it for us. For example
{% highlight python %}
unknown = something
print(unknown)
{% endhighlight %}
This script will print out the value unknow - any values unknown is!. That's fantastic, since we can always be aware and control the flow of our script. This is a feature which is not present in `C`, making `C` a harder language sometimes.

All right, for the moment that's all :) Hope you enjoyed it :)



