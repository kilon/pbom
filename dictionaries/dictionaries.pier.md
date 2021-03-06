

##Dictionaries



###1\. References

Before continuing to Dictionaries , I would like to explain a very important and fundamental concept of python that applies to pretty much anything\. Its a concept that is crucial to understand because if you don't you will come against problems that will be impossible to solve\. No worries though this concept is very easy to understand\.

When you assign a variable lets say a =1 or name= "john" its easy to assume that basically what is happening is that the computer finds an address in memory and stores there number 1 and assign the variable to that address and then finds another address in memory stores there the string "john" and assign this address to variable name\. So far so good\.

But if we then do variable b=1 and name2="john" we assume once more that previous process is repeated\. This assumption is wrong \.What it really has happened here is that the previous address that has stored 1 now is assigned to both a and b and the address that has stored "john" is assigned to both name and name2\. Ok so where is the problem ?

Lets try this



```python
list1 = ["one","two","three"]
list2=list1
```



this means that now list 2 is \["one","two","three"\] if we do



```python
list2[0]=1
```



this means that now list2 is \[1,"two","three"\] so far so good , but if we check list1 again list one is \[1,"two","three"\]

and if we do



```python
list1[0]="bazooka"
```



then of course list1 is \["bazooka","two","three"\] but also lists2 is \["bazooka","two","three"\]


This phenomenon is called "shared references" and it is used alot by Python in order to save memory\. Imagine what would happen if our program generated thousands of lists all of them having the exact same data , that would be mean using loads of memory while in this case shared reference means that we can save 1000 times more memory and of course it is absolutely crucial when your application deals with megabytes or even gigabytes of data\. One will ask how then we seperate the reference of list1 from the reference of list2, notice here that the entire list is referenced not just its indices\. On way doing this is by copying the data in case of list it can happen this way



```python
list1 = ["one","two","three"]
list2=list1[:]
```



if you remember we used \[0:2\] to spit a list but in this case because there is no start and end index the list is copied index by index and thus the copy returned is assigned in a different memory address and we can change it without affecting the original data\.

So this all was references, we will discuss how we deal with deep copies \(no reference\) and references in later chapters, but it is crucial you remember the basic concept and that it applies to pretty much anything data wise inside python\.



###2\.  Dictionaries

Dictionaries are by far my favorite type of data in python\. Actually I think they are the favorite type of python data for most python wizards out there\. Dictionaries are very similar to lists, like lists they store multiple types, like lists they are mutable so their data can be modified \. like lists they are accessed via index but unlike lists their indexes can be not only numbers but names as well\.

This is the basic syntax



```python
record = { "Name" : "James" , "Surname" :"Bond" , "age" : 32 , "license to kill": [0,23,12,45,67], 5 : "ok" }
print(record["Name"])
```



So there some things that are obvious from the start\.



- First ,that python knows that this is a dictionary because of \{ and \}
- Second, the index names also called keys are strings like "name"
- Third, a dictionary can contain a list
- Forth, the key is separated from its data using the : symbol\.
- the print will print the string value "James" , since that is what corresponds to keyword "Name"\.

You may ask why keys dont use names like \{name:"James"\] \. Because in this case python will actually try to search for a variable named name and use its data as a name for our key and this is not what we want here\.

Another advantage of dictionaries over lists is that the numerical indices are not in a sequence, so you have index 1 and 3 for example \(or more correctly key 1 and key 3\) but not index 2 \. This is useful when data is in not continuous\.

I dont want to go very deeply into dictionaries, we will use them later , but more or less this what they do and how they behave\.Two important functions you should remember is dict\.keys\(\) which return the names of the keys and dict\.values\(\) that returns only the values stored in the keys\. Observe that both functions use dot sign so that means they are members of the object of dictionary type so in the above example you would do record\.keys\(\) or record\.values\(\)
