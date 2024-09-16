java c
ITD102: Computer Technology Fundamentals
Workbook 2: High Level Technologies
This document contains the practical exercises questions relevant to the second part of this unit.
Raspberry Pi: All students need a Raspberry Pi. There is no textbook to purchase but you do need a Raspberry Pi. It’s important to obtain a Raspberry Pi soon – see the Raspberry Pi notes on Canvas for details, under Overview -> Things that you need. If you are an on-campus student you can borrow a kit containing everything that you will need from reception.
Students located overseas will need to source their own components.
MARKING: The practical exercises are competency based and will be checked by your tutor during the corresponding class or next class. Online students may instead submit a video of their demo with the same deadlines. All students need to demonstrate competency in the practical exercises; you may try multiple times (before the due date). The exercises are pass / fail – there are no part marks. The four practicals are worth 20% of your marks for AT2 (4 x 5%).
DUE DATE: All practical exercises must be successfully demonstrated to your tutor in person during your scheduled tutorial class on the week delivered or the following week at the beginning of the class; this also allows for public holidays. Late submissions cannot be marked.
These practical exercises should be done in a group of two (when possible), but you will be assessed individually.
Class 5: Languages and Libraries
The fifth lecture describes the two key methods by which we manage complexity in computer systems: high level programming languages and software libraries. These techniques are used extensively at all levels of a computer system from low level hardware and software to business processes and workflows.
In this class you will:
· Investigate programming language implementation techniques in practical exercises
· Explore programming languages and software libraries and APIs in the further work exercises
Practical Exercises
Use a command line shell on a Raspberry Pi for these exercises. You do not need to provide a written answer to these questions: rather you need to demonstrate competence to answer some of the questions to your tutor.
1. Compiling
Here is a very simple C program which prints out the text “Hello World”. Traditionally hello world is the first program people write and one which people like to see written in lots of different programming languages. C programs are typically compiled to machine code for execution on a particular kind of machine (CPU and Operating System).
// Hello World program in C
#include
main()
{
printf("Hello World");
}
a) Enter this hello world program into a file called hello.c e.g. using the nano text editor (your tutor will show you how). To run the program we must first compile it into machine code which the computer understands. Compile the program using the gcc compiler thus gcc hello.c . This will produce an executable machine code program in a file called a.out You can run this by entering ./a.out at the command prompt.
b) Rather than compiling your hello world program directly to binary machine code you can compile it to assembly code so you can view the textual representation of the machine code instructions. You can do that like this: gcc –S hello.c The assembly code will be put in a file called hello.s Look at this file (e.g. using nano), you should be able to find the text “Hello World”. You can carefully change this text, then convert the assembly file to machine code using gcc hello.s, then run the revised machine code using ./a.out as before. Congratulations - you’ve just programmed the computer in its own low level machine code language.
c) Look at the assembly code in hello.s, identify a machine instruction. Look up the instruction on the internet and find out what it does.
2. Interpreting
Here is a very simple python program which prints out the text “Hello World” and the length of this text. Usually the python language is implemented by translating to a simpler language (byte code) which is then interpreted by a program.
# Hello World program in python
print "hello world"
print len ("hello world")
a) Type the python program into a file called hello.py you can run the program by typing python hello.py 
b) Python runs programs by compiling them to an intermediate byte code language then interpreting this language (which lies between machine code which the computer can directly understand and the high level Python language). Python bytes codes are often written to files with a suffix .pyc. however these files are unreadable. To look at the Python byte codes for the hello world program use the following command: python /usr/lib/python2.7/dis.py hello.py
c) Choose a byte code instruction and investigate what it does (http://docs.python.org/2/library/dis.html)
3. JIT Compilation
The Java language uses JIT compilation: programs are compiled to bytecode using a compiler then later the bytecode can be run using a JIT compiler which compilers the bytecodes to machine code which is then immediately run. To complete this exercise you will need to install the Java SDK. You can do this by running:
sudo apt update
sudo apt install default-jdk
Here is a simple Java program:
public class hello
{
public static void main(String[] args)
{
System.out.println("Hello World!");
}
}
Put this in a file called hello.java; it must have that exact file name. The program can be compiled to bytecode (called a classfile in Java) thus:
javac hello.java
You can run the program using the Java JIT thus:
java hello
You can look at the bytecodes thus:
javap -c hello.class
Once you have completed these practical exercises individually demonstrate your understanding and competency to your tutor. You need your tutor to be satisfied that you have this new practical knowledge and skill in order to pass this module.
End of Class 5.
Class 6: The Web
The sixth lecture concerns the world wide web: what it is, how it evolved and how it works. The web is ubiquitous and has become the fabric which connects almost everyone for business, education, healthcare, government and leisure. Thus, it is important for everyone to understand the basics of how it works and how it is evolving.
In this class you will:
· Undertake practical exercises to understand how the web works and to investigate some web technologies.
· Understand the evolution of web technologies and some current web technologies.
Practical Exercises
You will need to use a command line shell on a Raspberry Pi for some of these exercises and a PC or Raspberry Pi with a graphical interface for other exercises. You do not need to provide a written answer to these questions: rather you need to demonstrate competence to answer some of the questions to your tutor.
1. HTTP Protocol: Web Clients and Servers
In this exercise we shall investigate how web clients e.g. browsers and servers work. You will need to be on the QUT network for these exercises.a) On Linux a useful command line tool for getting web pages is wget. Use wget to get some web pages and look at their HTML e.g. wget www.qut.edu.au2. Cascading Style.代 写ITD102: Computer Technology Fundamentals Workbook 2: High Level TechnologiesJava
代做程序编程语言 Sheets
You will need to do this exercise on a PC (or a Raspberry Pi using its graphical interface).a) Investigate cascading Style. Sheets (CSS). Use some different external style. sheets to style. a HTML web page in different ways. There are many CSS tutorials e.g.: http://www.w3schools.com/html/html_css.asp. This tutorial will let you interactively explore different features of CSS. If you have never written any HTML before you will need to read some of the earlier tutorials e.g. http://www.w3schools.com/html/html_intro.asp.
3. HTML 5
You will need to do this exercise on a PC (or a Raspberry Pi using its graphical interface).a)  Investigate some of the new features of HTML 5, for example the canvas element e.g. try some of the interactive exercises here http://www.w3schools.com/html/html5_canvas.asp. For more advanced HTML 5 fun see e.g. http://www.html5canvastutorials.com/ 
Once you have completed these practical exercises individually demonstrate your understanding and competency to your tutor. You need your tutor to be satisfied that you have this new practical knowledge and skill in order to pass this module.
End of Class 6.
Class 7: Security
The seventh lecture concerns computer security at the operating system, network and hardware level. The more our world becomes connected and automated the more important computer security becomes. Computer security affects all aspects of computer systems. This class focusses on some key technologies for securing computer systems.
In this class you will:
· Undertake some practical experiments with some of the security features in Linux including: file permissions, network security and encryption
· Investigate aspects of computer security as it applies to the home and enterprises
Practical Exercises
These exercises should be undertaken on a Raspberry Pi.
You do not need to provide a written answer to these questions: rather you need to demonstrate competence (evidence) to answer some of the questions to your tutor.
1. Linux file permissions
See: https://www.hostinger.com/tutorials/linux-commandsa) Investigate Linux file permissions, in particular create a file which can only be read and written by the user who creates it e.g. user “pi”. Use the chmod command to change the file permissions.b) You have written a convenient script. to print out useful system information:
#!/bin/bash
echo "Hello, $LOGNAME"
echo "Current date is `date`"
echo "User is `who i am`"
echo "Current directory `pwd`"
Put this in a file called sysinfo.sh and make the file executable using chmod, so that it can be run thus: ./sysinfo.sh You may find such scripts useful for your mini-project. We will discuss them further in the third module.
Hints: https://www.andrewcbancroft.com/blog/musings/make-bash-script-executable/
2. Public-key cryptography Watch and Discuss with group
https://www.youtube.com/watch?v=y2SWzw9D4RA
End of Class 7.
Class 8: Mobile, Cloud and the Internet of Things
The eight lecture discussed how Moore’s Law is giving rise to new classes of technology, including the cloud, mobile devices and the Internet of Things (IoT). This class is designed to lead into potential mini-projects and to show you how to make and understand some of the demos which have been shown in lectures, like the internet security camera.
In this class you will:
· Build one of:
o A simple mobile app, or
o A virtual machines, or
o A IoT device (this is a good basis for a mini-project)
· Investigate different technologies associated with mobile, cloud and the Internet of Things.
Practical Exercises
Undertake one of the following practical exercises. You do not need to provide a written answer to this question: rather you need to demonstrate competence to answer the question to your tutor.
1. Virtual Machines
Virtual machines (VMs) provide a way to separate operating systems from hardware. They are used in Infrastructure as a Service cloud computing systems like Amazon EC2. The Oracle VirtualBox VM system (www.virtualbox.org) is installed on PCs in the labs (if not you can install it yourself).a) What is a hypervisor?b) Investigate VirtualBox. How can you control the amount of memory and CPU time allocated to a virtual machine? Try changing the amount of memory and CPU allocated to e.g. an Ubuntu virtual machine and investigate the effects of doing so.c) Why might it be necessary to control the resources allocated to a virtual machine?d) Find where the disks and settings for virtual box VMs are stored. Try moving a virtual machine from one PC to another by copying the settings and disk onto a large usb memory key and then copying these onto a different machine from the usb key. Try running the VMs on the new machine – you have just manually migrated a virtual machine from one computer to another.e) Investigate the different networking options available with virtual machines.
2. Mobile apps
Use the app inventor system http://appinventor.mit.edu to build a simple mobile application. For example follow these instructions to make a magic 8 ball http://appinventor.mit.edu/explore/teach/magic-8-ball.html or select another simple/short exercise from here http://appinventor.mit.edu/explore/ai2/tutorials.html. You will need a google account in order to do this exercise and you will need to install the app inventor software on your PC (or Android device). The key to this exercise is to carefully follow the instructions. Feel free to create your own app or embellish an existing one. You can run programs either on the emulator or on your Android phone, if you have one. Show your finished application to your tutor.
3. Internet of Things
Note these exercises are particularly suitable starting points for mini-projects. There are many cloud services for IoT devices. They enable you to connect devices to its cloud based service to control and monitor them and collect data. Here is a list of some popular IoT services which you can connect your Raspberry Pi to:· Sparkfun data service: https://data.sparkfun.com/ tutorial:https://learn.sparkfun.com/tutorials/pushing-data-to-datasparkfuncom/raspberry-pi-python · Grove Streams https://grovestreams.com/ tutorial https://www.grovestreams.com/developers/getting_started_rpi.html · Thingspeak https://thingspeak.com/ tutorial https://www.dexterindustries.com/BrickPi/brickpi-tutorials-documentation/projects/thingspeak-temperature-log/ · Adafruit IO  https://io.adafruit.com/ tutorial https://learn.adafruit.com/adafruit-io-basics-neopixel-controller 
You may need to adapt some of these tutorials e.g. to upload something local. For example an interesting built-in sensor is the Raspberry Pi CPU temperature sensor which can be accessed from the command line thus: /opt/vc/bin/vcgencmd measure_temp
Another alternative is to investigate how to upload a file to dropbox from the raspberry Pi e.g. upload a photo. https://www.raspberrypi.org/magpi/dropbox-raspberry-pi/ 
Once you have completed these practical exercises individually demonstrate your understanding and competency to your tutor. You need your tutor to be satisfied that you have this new practical knowledge and skill in order to pass this module.
End of Class 8.





         
加QQ：99515681  WX：codinghelp
