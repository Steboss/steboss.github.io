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

# Gaining Python!


First of all we have to download python from [here].
![PythonDownload]({{site.url}}/assets/2017-07-20/PythonDownload.png)


Rather than downloading the latest Python release, it's better to download the Python which suits best for your laptop.
If you have a 64 bit laptop and you want the newest Python, so download **windows x86-64 executable installer**, otherwise for 32 bit computers **windows x86 executable installer**.

Once the download has finished click on the installer and a windows like this will pop up:
![PythonInstall1]({{site.url}}/assets/2017-07-20/1.jpg)


Click on **Customize Installation** and an _optional features_ window will appear :
![PythonInstall2]({{site.url}}/assets/2017-07-20/2.jpg)


This should be totally fine or check the same options I have checked, and click on _next_.
The third windows is **really important: Advanced Options**:
![PythonInstall3]({{site.url}}/assets/2017-07-20/3.jpg)


Here you have to tell the install to install python in ```C:\Python36```, where ```C:``` is your hard disk
device name and ```Python36``` the name of the folder where we want to install Python. This folder will be created during the installation and you can choose the name you most prefer for it.

Finally, click on **Install** and the installation process will start:
![PythonInstall4]({{site.url}}/assets/2017-07-20/4.jpg)


and should finish in 10 minutes max - with a big thanks to Mark Hammond
![PythonInstall5]({{site.url}}/assets/2017-07-20/5.jpg)


## Make Python great in prompt!

Now you have a new folder on your laptop, maybe in ```C:\Python36```, with all the materials and stuff to run pyhton. However, at the moment you can't do so much with your Python idle. Once you have written a script you would like to run it whereever you are on your computer. Executing a Python script can be done in two ways: 
calling the Python interpreter with a command line or using the interactive Python shell. For now on we will adopt the first option and we will use our Python scripts using the **command prompt** of Windows. In this way, we could use the command prompt and typing ```python``` and being able to use it both to run a program or to code.


To use the command prompt without any problem we need to set a _variable_ . A variable is a path of a program, for example ```C:\paint\paint.exe```. Thus, to set the Python variable we need to go to **Advanced System Settings** 

Then, click on **Environment Variables**. Under the voice **User Variables** click on ```Add``:
![PythonInstall6]({{site.url}}/assets/2017-07-20/6.jpg)


Set the new User Variable Name to **PATH** and  copy and paste this stringC:\Python36;C:\Python36\Lib\site-packages\;C:\Python36\Scripts\;C:\Python36\DLLs;C:\Python36\Include;C:\Python36\python.exe``` into **Variable Value***. Be careful, modify each ```C:\Python36``` if you have installed Python in any another folder.

Give all the possible OKs and go to the prompt command:
![PythonInstall6]({{site.url}}/assets/2017-07-20/6.jpg)

By typing ```python``` you will be able to access to the python idle. We will see very soon the powerful of such a method!
