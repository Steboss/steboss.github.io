---
layout: post
title:  "Installing Python on Windows"
date:   2017-07-20 11:18:48 +0100
categories: basic-python
---

Due to the 'cheap' price of a MacBook, many of us are relying on a Windows computer.
Not bad, Windows nowaday is fast, reliable and portable. The main drawback is the absence of Python 
in the operative system.
Therefore, today we will see how to install Python in Windows :) 

First of all we have to download python from [here].
![PythonDownload]({{site.url}}/assets/2017-07-20/PythonDownload.png)
Rather than downloading the latest Python release, it's better to download the Python which suits best for your laptop.
If you have a 64 bit laptop and you want the newest Python, so download **windows x86-64 executable installer**, otherwise for 32 bit computers **windows x86 executable installer**.

Once the download has finished click on the installer and a windows like this will pop up:
![PythonInstall1]({{site.url}}/assets/2017-07-20/1.jpg)
Click on **Customize Installation** and an __optional features__ window will appear :
![PythonInstall2]({{site.url}}/assets/2017-07-20/2.jpg)
This should be totally fine or check the same options I have checked, and click on __next__ .

The third windows is **really important: Advanced Options**:
![PythonInstall3]({{site.url}}/assets/2017-07-20/3.jpg)
Here you have to tell the install to install python in ```C:\Python36```, where ```C:``` is your hard disk
device name and ```Python36``` the name of the folder where we want to install Python. This folder will be created during the installation and you can choose the name you most prefer for it.

Finally, click on **Install** and the installation process will start:
![PythonInstall4]({{site.url}}/assets/2017-07-20/4.jpg)
and should finish in 10 minutes max - with a big thanks to Mark Hammond
![PythonInstall5]({{site.url}}/assets/2017-07-20/5.jpg)


You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
[here]: https://www.python.org/downloads/windows/