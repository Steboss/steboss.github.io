---
layout: post
title:  "Taming loops! - Part 2"
date:   2017-07-23 14:39:48 +0100
categories: basic-python
---

I hope you enjoyed the `for` loop part. Today, we are going to deal with `if-clause` loop. 

# If clause

As I wrote before, the `if` loop check if a variable holds a specific condition. If that variable is ok we will do something, otherwise we will do something `else`. 


# If in action

Using your favourite text editor write this script:
{% highlight python %}
i = 8
if i<5 : 
    print("%d is less than 5" %i)
elif i > 5:
    print("%d is greater than 5" %i)
else:
    print("%d is something else" % i)
{% endhighlight %}

save it as `ifclause.py` and run it. Obviously the output will be `8 is greater than 5`. Nothing special, but it's useful to analyze and learn what a `if clause` does and works:

- `if i<5:` : the `if` condition starts with `if` and a condition to be held. Remember the columns `:` at the end

- `    print("%d is less than 5"%i)`: secondly, take care of the indentation - `tab` - and `if i is less than 5` we will print out this message

- `elif i>5: ` : `elif` is an optional argument we can add to the `if` condition: if the first condition isn't true check the second condition, which starts with `elif`

- `else:` : finally, if all the conditions above don't work do something `else`

At the and the `if` cycle will be:
{% highlight python %}
if some condition:
    do something
elif  second option:
    do something
elif third option:
    do something
...
elif n-th option:
    do something
else:
    do something else
{% endhighlight %}

Another important example, which will be frequent in your projects, is coupling a `if` and `for`:
{% highlight python %}
for i in range(0,1000):
    if i<5 : 
        print("%d is less than 5" % i)
    elif i > 100 : 
        print("%d is greater than 100" % i)
    else :
        print("%d is a number, no doubts" % i)
{% endhighlight %}

In this case `i`, our variable, will go through a range of value. At any time we are giving a condition to be respected and something will be printed out.

Finally, it may be that sometimes we do not want to do anything on a variables if the condition is not held. thus we can use the command `continue`:
{% highlight python %}
for i in range(0,1000):
    if i<5:
        print("%d is less than 5" % i)
    elif i>100:
        print("%d is greater than 100" %i)
    else:
        continue
{% endhighlight %}

What will be the output of this script?

Now, it's time to add some spices to our code and coupling cycles with user input variables. One lovely aspect of coding is to interact with the code itself. There are many ways to do that and one of the is to use the Python module `sys`. 

# Ginger on the code : modules

Any code language is made up of `libraries`. Each library has a define set of functions that the user can adopt to play with the code. One of the most known library in `C` is `stdio.h`. This is the standard library and contains all the function to `print`, `scan`, so read the user input and so on. In Python `print` function is already on in the Python interpreter. The same for `scan` which is called `raw_input`. Anyway, today I would like to talk with you about a more important input which is given by the `sys` library or module Pyhton.

Open a new file and type:
{% highlight python %}
import sys

number = int(sys.argv[1])

if number<0:
    print("%d is negative" %number)
elif n> 100:
    print("%d is greater than 100" % number)
elif n==1000:
    print("%d is equal to 1000" % number)
else:
    print(" %d is definitely a number" % number)
{% endhighlight %}

Save it as `if_input.py` and run in the prompt in this way:
ADD A FIGURE
`python if_input.py  100`

What's going on? Let's analyse the code:
- `import sys` : this is new. `import` states for "import something in my code", namely import a library, a function or a script. `sys` is the name for the sys module (there will be a lot of funny [exercises][sysexercises] about that). Once sys is imported we can use all the function of the sys library by typing: `sys.function`, where function is a specific command of sys

- `number = int(sys.argv[1])`:  This is the input given by the user. As you can see when we were running the code we typed in the prompt `python if_input.py 100`. `100` is the input we are giving the code. This input is read by `sys.argv[1]`. `sys` is the module we are using; `argv` means `argument variables` and it's saying to the code that there will be an input. Where is the input? In position `1`. What does that mean? 
Basically, Python has a way to recognize the inputs with sys based on this scheme:
`python SCRIPT [Position:0]  INPUT_1 [Position:1] INPUT_2[Position:2] ... INPUT_N[Position:N]`
thus right after the script we will write the input argument. Finally `int` is a way to convert the number we have given into an integer. For example: `int(100)` returns `100` and `int(12.3)` return `12`. 

- After the input is given we are going to play with it with some conditions

All right :) 
now we know really a lot and we can start to code a bit more. Let's try to deal with some [exercises][ifexercises] 

[ifexercises]: ifexercises.html