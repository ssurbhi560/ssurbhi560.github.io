---
layout: post
title: "Python Session on Slack"
date: 2019-9-13
---

The first session of our training to open source contribution was scheduled on 15 September 2019 at 12:30 pm on slack.

After joining for the session on slack, everyone was instructed to login and open jupyter notebook. It's a web based interactive environment for running python ( the link for which was sent already before the session).
  
So session started with Rahul telling everyone that **Why one should even learn python?** Answer to which was that if you know Python, you can do just about anything from web development, testing, machine learning and data science, GUI development, server side development, data visualisation, anything. Amazing right? XD
Okay but that just counts the pros of python but now let's look upon some cons, one of this is that python is slow in terms of the code execution time. But for developers what is more important is the time that they invest in writing the code which is way too fast in python than any other programming language, so python wins!

After that we started using python, first used it like a calculator and learned some basics, then some functions like `print` was introduced and we finally wrote this -

```print (Hello, World) ```

Then we moved further by taking up some more basics like data types, variables, escape characters etc. to a little difficult topics like how to take an input from user, how to chnage one data type to another, conditional statements, importing libraries, using `exit() ` when we don't want the code to execute after a particular condition etc. During the session we had to write a program to solve a quadratic equation. 
To me initially, it felt like a little crowded , because of all the students asking so many questions but actually that was a good thing. After some time I got used to that and could easily follow all with all the things.  

Finally we wrote the program to find the roots of a quadratic equation. Because I already knew python so it was not much difficult for me, but the way it was told by Rahul, explaining all code line by line, every logic, anyone with no prior experience with any programming language must have been able to follow him without much difficulty. Also anyone could ask any questions or doubts during the session and every question was answered immediately so it was kind of very interactive session. We learned by doing the things which usually don't happen in normal classes. 

At the end of the session a assignment was also given for better understanding of the concepts.

**Assignment question** :
We have to write a program to solve quadratic equation which takes in the values of a, b, c as floats and also handles zero divisional error when a=0.

My solution to which is here: 

```
#code for finding the solutions of quadratic equation
import math as m
print("we'll be solving a quadratic equation : ax^2+bx+c=0.")
a = float(input("Please enter the coefficient of x^2: "))
b = float(input("Please enter the coefficient of x: "))
c = float(input("Please enter the value constant in equation: "))
det = (b**2-4*a*c)
if(a>0):
    if (det>0):
        print("Determinant is positive so roots are real.")
        print("The solutions of the given equation are:",(-b+m.sqrt(det)) , (-b-m.sqrt(det)))
    elif (det==0):
        print("Determinant is zero roots are equal.")
        print("The solution of the given equation is:", -b/2*a)
    else:
        print("Determinant is less than zero so roots are complex.")
        print("The solutions of the given equation are: ", (str(-b)+"+"+"i"+(str(m.sqrt(-det)))),(str(-b) +"-"+"i"+(str(m.sqrt(-det)))) )
else:
    print("The coefficient of x^2 should be greater than zero")
```