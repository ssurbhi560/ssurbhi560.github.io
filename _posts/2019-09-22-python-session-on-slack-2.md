---
layout: post
title: "Python Session on Slack - 2"
date: 2019-9-22
---
We had our second python session today at 2:00 pm.
Before starting the session @RJ722 first talked about - how the art of asking question is an important aspect of learning anything . 
[Here]( https://fs.blog/2012/01/richard-feynman-on-why-questions/  ) is something which you must read for that.  

In the session we were basically going to create an ID generating system , complete with an authentication system. In which you can enter the password to authenticate. Then you'll be entering the details of the person whose ID is to be generated and finally the ID gets printed on the screen. Awesome right, so let's start! \0/

So, to do this we had to cover the following topics in python:
-Looping
-Reading/Writing something from/to a file. 
-Functions in python.
-Hashing

We session started with discussion on loops, so "why do we need loops at all?" the answer to which is, sometimes when we need to do something repeatedly, loops makes our life easier. Two popular loops in Python are- ``while`` and ``for`` loop. We generally use a ``while`` loop, when we don't know how many times exactly, does the loop need to be run and ``for`` loops are used when we know exactly how many times do we need to run the loop. We also did some examples using these loops. 

Then we discussed lists- it's a data type in python same as we have arrays in C/C++, the only difference being that lists can have heterogeneous data. 

Then we were also introduced to `range` and `len` functions. The `len` function returns the length of anything (lists, tuples, dictionaries, etc.). `range` function is used to generate a sequence of numbers over time. 

After that we learned, how to read files using ``f.readlines`` , ``f.readline`` and ``f.read``, and to open the files in different modes- 
  'r' mode(read mode),
  'w' mode(write mode) and 
  'a' mode(append mode).

Then we moved further to talk about functions. 
"How to define a function?" and "Why functions are important?" 
So, let's answer these questions-
The way we define functions in Python is using the following syntax:

```
def function_name(argument1, argument2):
    print(..)
    return argument1 + argument2
```
And they are important because using these, we can reduce repetition of code. Then finally, we started working on the ID generator. The things that we needed to take care of, while making the id generator were:

-To validate that the user is actually entering correct names. For this we used ``isaplha`` function (this returns True if the characters are only alphabets, otherwise returns False)

-To keep the passwords secure and safe- we used hashing and to do so we used libraries **getpass** and **hashlib**.

-To make it more readable, we used **texttable**. This is another Python library for printing tables in a pretty format.

There's a library for almost anything and everything in Python!! xD 
We also added a logo of AMU-OSS to make our ID generator look more real and cool. 

You can go through the complete code [here](https://nbviewer.jupyter.org/github/amu-oss/id_gen/blob/master/id_gen.ipynb)

So the session ended here and the students were also given an assignment which was to find out why we called main() function in this way -

```
if __name__ == '__main__':
    main()
```



