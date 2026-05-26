+++
title = "Python Workshop Resource & Installation Guide"
date = "2025-09-19T12:00:00+10:00"
author = "Swinux Committee"
description = "Have you ever wanted to learn how to code? This article explains the basics to get you started on your coding journey with Python."
readingTime = true
tags = ["article", "code", "guide"]
+++

Have you ever wanted to learn how to code? This article explains the basics to get you started on your coding journey with Python. This will get you to a point where you can follow along with the workshop.

If you haven't yet, [join our club](https://campus.hellorubric.com/?s=12119) and [our discord](https://discord.gg/ZfCW8DhnhA)! This will allow you to chat with other Swinburne students interested in Computer Science, who will be happy to give you all sorts of tips and tricks as well as help if you're stuck.

# Setting Up Your Computer

First, we need to establish some terms so you know what we're talking about:

- **Console/Terminal/CMD**: This is what we use to run our programs. It's simple and it's entirely text-based (like the hackery things you see in the movies) but it means you can type *exactly* what you want, and your computer will do it. It may seem daunting, but you will get used to it quick smart.

- **Program/App**: This is what you will run in the console, which will execute (run) your code, giving you an output. In the workshop, it will be saved as a single .py file. You can have multiple files but you will only run one at a time.

- **Directory/Folder**: This is the layout of where files on your computer are stored. A Directory can be a single folder, or many folders together to point to a specific area where files are stored.

- **Operating System (OS)**: There are three major Operating Systems, Windows, Mac and Linux. Each one may have a different way of setting things up. Where they are different, we will write specific instructions for you to follow.

Before we even start coding you'll need to install Python. It's an accessible and readable programming language developed in 1991. You'll find out exactly why it's so accessible and readable soon.

[Click here for the Windows installation steps.](https://swinux.org/posts/learning-python/post/#installing-python-on-windows)

[Click here for the Mac installation steps.](https://swinux.org/posts/learning-python/post/#installing-python-on-mac)

[Click here for the Linux installation steps.](https://swinux.org/posts/learning-python/post/#installing-python-on-linux)

[Other Workshop Resources](https://swinux.org/posts/learning-python/post/#resources)

## Installing Python on Windows

Official Windows Python Install Guide: https://docs.python.org/3/using/windows.html

If you're on a regular x64 laptop (Almost everyone) visit https://www.python.org/downloads/release/python-3137 and install the Windows Installer (64-bit) program.

If you're using a Snapdragon laptop, visit the above link and install the Windows Installer (ARM64) program.

![Downloading Python on Windows](/posts/learning-python/images/windows/step1.png)

Scroll down the page a bit until you see something similar to the image below. Remember what platform you're on and download the appropriate file.

![Downloading Python on Windows](/posts/learning-python/images/windows/step2.png)

Wait for the file to download. Once it's download it should look something like this:

![Downloading Python on Windows](/posts/learning-python/images/windows/step3.png)

Navigate to your downloads folder and double click on python-3.13.7-amd64.exe or python-3.13.7-arm64.exe (Depending on what you downloaded) to run the installer:

![Downloading Python on Windows](/posts/learning-python/images/windows/step4.png)

Click the 'Install Now' button and wait for Python to install itself. Once you reach the 'Setup was successful' screen, exit the program.

![Installing Python on Windows](/posts/learning-python/images/windows/step5.png)

![Installing Python on Windows](/posts/learning-python/images/windows/step6.png)

![Installing Python on Windows](/posts/learning-python/images/windows/step7.png)

Press the Windows button on your keyboard and type cmd. An app called Command Prompt will appear. Open Command Prompt.

![Run Python on Windows](/posts/learning-python/images/windows/step8.png)

![Run Python on Windows](/posts/learning-python/images/windows/step9.png)

At this stage, your desktop should look similar to the image above. This is what you will use to run the Python programs we create in the workshop. For now, set it aside and move on to the 'Your First Program' section. If you face any issues, use the [Official Windows Python Install Guide](https://docs.python.org/3/using/windows.html).

[Click here to jump to the next section.](https://swinux.org/posts/learning-python/post/#using-windows-to-run-python-code)


## Installing Python on Mac

Official MacOS Python Install Guide: https://docs.python.org/3/using/mac.html

To download the Python installer, navigate to https://www.python.org/downloads/release/python-3137 and look for the macOS 64-bit universal2 installer and download it, seen below.

![Downloading Python on Mac](/posts/learning-python/images/mac/step1.png)

Make sure this is the file you download:

![Downloading Python on Mac](/posts/learning-python/images/mac/step2.png)

Once it has downloaded, double click on the file to launch the installer:

![Downloading Python on Mac](/posts/learning-python/images/mac/step3.png)

Navigate through the launcher to install Python:

![Downloading Python on Mac](/posts/learning-python/images/mac/step4.png)

![Downloading Python on Mac](/posts/learning-python/images/mac/step5.png)

![Downloading Python on Mac](/posts/learning-python/images/mac/step6.png)

Once that is complete, Python is installed and you should see the following prompt:

![Downloading Python on Mac](/posts/learning-python/images/mac/step7.png)

However, you now need to install a certificate to allow Python to work correctly.

Navigate to the `Applications/Python 3.13/` directory to view the following contents:

![Downloading Python on Mac](/posts/learning-python/images/mac/step8.png)

Double clicking on the .command file will allow Python to run correctly. You should be able to see the following prompt within a terminal window:

![Downloading Python on Mac](/posts/learning-python/images/mac/step9.png)

When this is complete, you can open the terminal app. If you type the below command and press enter, you should see Python and it's version number.

`python --version`

At this stage, Python should be installed correctly. This is what you will use to run the Python programs we create in the workshop. For now, set it aside and move on to the 'Your First Program' section. If you face any issues, use the [Official MacOS Python Install Guide](https://docs.python.org/3/using/mac.html).

[Click here to jump to the next section.](https://swinux.org/posts/learning-python/post/#using-mac/linux-to-run-python-code)

## Installing Python on Linux

Look at you. You're already using Linux, you shouldn't need to be told how to install Python. You probably already have it installed out-of-the-box.

If you *really* want to install it again, open the console and type the following, depending on your distribution:

Debian-Based Distributions
`sudo apt install python`

Fedora-Based Distributions
`sudo dnf install python`

Arch-Based Distributions
`sudo pacman -S python`

Nix/Gentoo-Based Distributions
`Have fun.`

[Click here to jump to the next section.](https://swinux.org/posts/learning-python/post/#using-mac/linux-to-run-python-code)

# Using Windows to run Python code

Once you've got python installed, you can verify that it is in fact ready to run by using the following command in the console:

For **Windows**:

`py --version`

![Running Python on Windows](/posts/learning-python/images/windows/step10.png)

It should print Python 3.XX.X to the screen, with X being the specific version numbers of the program.

You can now create your first application using your favourite text editor (such as notepad+++ on Windows).

To keep your disk nice and clean, we reccomend creating a seperate folder just for Python files. On all Operating Systems, create a folder called Python in your Documents folder.

Name it `myfirstprogram`, as it's the first program you've ever made! Make sure not to append .txt to the file, as Python will not be able to find and run it. You need to append .py to the file so Python will recognise it as a Python program that can be used.

Once you're ready to edit the file, add the following:

![Running Python on Windows](/posts/learning-python/images/windows/step11.png)

Save the file, and get ready to run the program. Using the console, navigate to the folder/directory where the python file was saved.

On **Windows**, you can do the following (Keep in mind the folders must exist, and your Python file should exist in that folder/directory):

`cd "C:\Users\yourusername\Documents\Python"`

Once you've done that, you should be in the correct folder. Run the command below:

`py myfirstprogram`

You should have seen a 9 get printed to the console on your screen. That means that you've just ran your first program!

![Running Python on Windows](/posts/learning-python/images/windows/step12.png)

If you don't see that, make sure you've got Python installed and that you've copied the code exactly, otherwise it may not run as you'd expect. Python is pretty good with telling you exactly what went wrong and where it happened, but it won't necessarily tell you how to fix it. This is where the resources section below will help you with your understanding.

At this point, you are ready for the workshop. Please follow along with the coding examples during the workshop to get the most out of it, either on your device or via the slides.

[Workshop Resources](https://swinux.org/posts/learning-python/post/#resources)


# Using Mac/Linux to run Python code

Once you've got python installed, you can verify that it is in fact ready to run by using the following command in the console:

For **Mac/Linux** (Linux example provided):

`python --version`

![Running Python on Mac/Linux](/posts/learning-python/images/linux/step1.png)

You can now create your first application using your favourite text editor (such as notepad+++ on Windows).

To keep your disk nice and clean, we reccomend creating a seperate folder just for Python files. On all Operating Systems, create a folder called Python in your Documents folder.

Name it `myfirstprogram.py`, as it's the first program you've ever made! Make sure not to append .txt to the file, as Python will not be able to find and run it. You need to append .py to the file so Python will recognise it as a Python program that can be used.

Once you're ready to edit the file, add the following:

![Running Python on Mac/Linux](/posts/learning-python/images/syntax.png)

Save the file, and get ready to run the program. Using the console, navigate to the folder/directory where the python file was saved.

On **Mac/Linux**, you can do the following (Keep in mind the folders must exist, and your Python file should exist in that folder/directory):

`cd ~/Documents/Python`

Once you've done that, you should be in the correct folder. Run the command below:

`python myfirstprogram.py`

You should have seen a 9 get printed to the console on your screen. That means that you've just ran your first program!

![Running Python on Mac/Linux](/posts/learning-python/images/linux/step2.png)

If you don't see that, make sure you've got Python installed and that you've copied the code exactly, otherwise it may not run as you'd expect. Python is pretty good with telling you exactly what went wrong and where it happened, but it won't necessarily tell you how to fix it. This is where the resources section below will help you with your understanding.

At this point, you are ready for the workshop. Please follow along with the coding examples during the workshop to get the most out of it, either on your device or via the slides.

[Workshop Resources](https://swinux.org/posts/learning-python/post/#resources)

# Resources

Below are links for the workshop, including slides and full code examples:
- [Google Drive](https://drive.google.com/drive/folders/1F5smICawa9SviFuLLddfIBlY2cNIq6xU?usp=drive_link)
- [Rubric Fileshare](https://admin.hellorubric.com/files?id=002b880e-f75a-4202-8e22-1ffe00953616)

We've prepared some resources for you which may assist you in learning how to program. Some of these resources focus on other programming languages, but the principles are useful and may give you some ideas of projects to attempt.

- [W3Schools](https://www.w3schools.com/python/default.asp), A collection of resources for learning Python, alongside other languages. Features a browser-based interactive code editor.
- [Pip](https://pip.pypa.io/en/stable/), A Python library package manager to install libraries for use in your programs.
- [The Coding Train](https://www.youtube.com/@TheCodingTrain), an enthusiastic programming teacher that builds and explains creative and interesting projects. 
- [FreeCodeCamp.org](https://www.youtube.com/@freecodecamp), an organisation providing lecture-style videos for all things programming, including Python.







