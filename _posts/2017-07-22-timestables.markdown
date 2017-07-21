---
layout: post
title:  "Taming loops! - Part 1- Timestables"
date:   2017-07-22 14:39:48 +0100
categories: basic-python
---

# Times 5 Exercise Answer

{% highlight python %}
for i in range(1,10):
	#the range can be modified as you like
   	for j in range(1,10):
   		#but must be same as above
   		product = i*j
   		print("%d times %d equals %d" %(i,j,product)) 
{% endhighlight %}

or if you prefer:

{% highlight python %}
#create an empty string
outline=""
for i in range(1,10):
	#the range can be modified as you like
   	for j in range(1,10):
   		#but must be same as above
   		product = i*j
   		#fill the string with product at each iteration
   		outline+="%d  " % product
   	#once the j is finished start a new line
   	outline+="\n"
#print everything
print(outline)
{% endhighlight %}

and what if we want to be tidier?
{% highlight python %}
#create an empty string
outline=""
for i in range(1,10):
	#the range can be modified as you like
   	for j in range(1,10):
   		#but must be same as above
   		product = i*j
   		#fill the string with product at each iteration
   		outline+="%d\t" % product
   		#here we added a tab between each number
   	#once the j is finished start a new line
   	outline+="\n"
#print everything
print(outline)
{% endhighlight %}