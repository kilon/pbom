

##Lists

You may think that since we got integers and floats and strings we have pretty much finished with Data types\. However python is a huge programming language, there is ton of stuff available \. Of course the goal of this book is not to teach you all of python just enough to get you started and working with blender so we will keep things as simple as possible\. However there are still some types that even though they are not absolutely necessary for making a working program they are absolutely necessary for keeping code simple and short\. One of those types is list\.

I can hear you wondering whether a variable can be assigned not one but several values\. Lists do exactly that\. Actually lists work very similarly to strings\. Lets see how we assign a list to variable\.



```python
a = \[ 1, 2, "hello" ,4 , 5.0 \]
print(a)
print(a\[2\])
```



a variable is assigned a list and we know its a list because we start the declaration with \[ and end it with \]\. Its important for python to recognize that this is a list because list are not the only way to assign multiple values to a single variable\. Lists work similarly to strings in a sense that we access them via an index, a\[x\] will return the value of variable a from index x \. In this case its clear that index 2 contains the string "hello" \. Remember what we said earlier 0 is always first for computer so here value 1 is in index 0 , that is why "hello" is in index 2\.

ok lets do the following



```python
a = "hello"
a\[0\] = "y"
```



It gives this error \-\-> TypeError: 'str' object does not support item assignment\. Basically it says we are not allowed to assign value in a string in a specific index\. Why ? Because strings are immutable , or read only\. Remember the string is immutable not the variable if we add to the previous example a = "yello" its perfectly ok\.

One may wonder why python implements mutable types that can be changed but also immutable types that cant be changed\. The reason is of course to provide means to protect values the same way some of your files in your system are read only \. Because they are very important files and you dont want anyone or anything messing with those files\. The same happens with data inside a python module\.

This is where a list comes handy because list is mutable and thus it can be changed\.



```python
a = "hello"
b=list(a)
b[0] = "y"
print(str(b))
print("".join(b))
```





so we assign a the string "hello" , b is assigned the value of a after it has been converted to a list , we can now change the h to y because lists are mutable but when we convert b back to string and print it we get spaces between and also "[" "," and "]". This happens because python converts the full declaration of the list to a string, but we dont want that . We want only the values joined together in a single string. So we use the function join.

You will observer here the weird dot between "" and function join. Types in python are objects and objects are groups of both data and\/or functions. Actually there are alot of functions we can use for each types some are part of their object some are just built in functions so they dont need a dot in the syntax. Dont worry about objects right now and how they work we will talk about them when we explain Object Orientated Programming.

Lets see some cool functions about lists




```python
names  = \["john" ,"mary" ,"peter" \]
names.append("jane")
print(names)
Append is member function of the object list , and of course it appends another index to the list. Observe that we use the dot to access the function. We can also split lists.

names  = \["john" ,"mary" ,"peter" \]
names = names\[0:1\]
print(names)
```



in this case it prints \['john'\] \. Observe that we dont use a second variable as names is reassigned the result of the split\. However now names has lost its previous values\. \[0:1\] means give me the indexes started from index 0 and ending on index 1 , index 1 is not included\.

Another cool thing about lists is that they can be multidimensional , there is no limit to how many dimensions a list has\. For example lets create a 3d list\.



```python
data3d = \[ \[\["x1"\],\["x2"\],\["x3"\]\] ,
           \[\["y1"\],\["y2"\],\["y3"\]\] ,
           \[\["z1"\],\["z2"\],\["z3"\]\] \]
print(data3d\[0\]\[1\]\[0\])
```



The comma allows us to use multiple lines for this one statement making our code easier to read\. Basically each dimension is a list inside another list for example this \[\] is one dimension list this \[\[\]\] is a 2d list this \[\[\[\]\]\] is 3d list and so on \. So \[0\]\[1\]\[0\] means the first sub\-sub\-sub list from the second sub\-sub list from the first sub list\. It may get abit confusing to understand multidimensional lists so its better that you do your own tests to make sure you have a good feeling about it because multidimensional lists is something that you may use several times in blender as their advantages are obvious\. The important thing to remember is that a dimension is just a list inside another list\.

Bare in mind that when accessing a list the dimensions are optional for example using the above source code we could do data3d\[0\]\[1\] or just data3d\[0\]\. Try it and get a feel of how a list really works\. There is no hurry , take your time\. These foundations you build now they will help a lot in the future\. There are many more things that can be done with lists , but I wont go to full detail, I only care of giving you basic knowledge but if you want to learn more you can visit the official documentation here\.




###1\.  Tuples

Tuples behave like lists the big difference is that they are not mutable so they cannot be changed , so they are preffered for sensitive data that should not change\. This is how you define a tuple



```python
names  = ("john" ,"mary" ,"peter" )
print(names)
```



Line 1 is not a function because even though it has open , close parentheses and parameters that are separated via commas there is no name in front of the parentheses so this way we know its a tuple and not a function\. Tuples like lists are accessed via index exactly the same way and like lists they can be multidimensional\.
x


```python
data3d = ( (("x1"),("x2"),("x3")) ,
           (("y1"),("y2"),("y3")) ,
           (("z1"),("z2"),("z3")) )
print(data3d[0][1])
```


