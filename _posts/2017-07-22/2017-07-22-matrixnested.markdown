---
layout: post
title:  "Taming loops!"
date:   2017-07-22 14:39:48 +0100
categories: basic-python
---

# Matrix Exercise Answer

{% highlight python %}
outline = ""
for  i in range(1,4):

    for j in range(1,4):

        element = i*j
        outline+="%d," % element

    outline+="\n"
 
 print(outline)

{% endhighlight %}
