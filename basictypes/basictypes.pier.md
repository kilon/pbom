

##Basic types

We will be using the intepreter's command prompt ">>>" to enter python command to help us understand the basic types that python uses to store data\.



###1\.  Integer type

Type the following command



```python
>>> 1+2
3
```



This a command containing and manipulating data\. The data is "1" and "2", and the command is "\+"\. "\+" is also called an "operator", a mathematical operator in this case\. What you see in the second line is the returned result which is of course "3"\. Python includes addition, subtraction, multiplication, and division mathematical operators\.

example of multiplication:



```python
>>> 2*3
6
```



example of division:



```python
>>> 6/3
2.0
```



example  of subtraction:



```python
>>> 2-1
1
```





###2\.  String type

Another Python command that can be used is the print\(\) command\. Below is an example of using the print\(\) command:



```python
>>> print("this is pure python magic")
this is pure python magic
```



This Python command is called a "function"\. This is considered a function because it includes a name, print, and opening and closing parentheses\. That is the basic syntax for any Python function\. However, it's not necessary to worry about what a function is exactly, for we will deal with it later\.

The "this is pure Python magic" is called a string\. What exactly is a string? Type the following into the Python Console, and then press enter toe execute the command:



```python
>>> "1" + "2"
'12'
```



As shown above, the output is the string '12'\. String can be represented with single quotes or double quotes\. Why is this? Because the command was not 1 \+ 2, but "1" \+ "2"\. Since quotes surround each number, they are considered strings\. Therefore, when using the addition operator, it combines the 2 strings into one string\. That being said, "1" \+ "2" becomes "12"\. Now, type "1" \* "2" into the Python Console, and press enter to execute the command\.



```python
>>> 1" * "2"
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can't multiply sequence by non-int of type 'str'
```



The output result in what is called a "Python error"\. Python errors are bad\. Everyone wants to type perfect code, and nobody wants to experience all the pain of correcting mistakes\. However, the world isn't perfect, and Python helps by reporting what is wrong\.

The error may seem a bit cryptic, but it's not hard to decipher\. The first line reports an error that was found, the second line reports where the error is, and the third line reports what the error is\. In this case, the error is TypeError\. "TypeError" means there is an error with the type\. When reading the rest of the line, it becomes obvious that it expected data type "int", but it got data type "str", which is short for string\. A string is a 'string' of characters, one character after another\. The "int" data type, short for integer, is one of the many types of numerical data\. Types matter a lot for all programming languages\. However, Python tends to be more forgiving with mixing different types in the same command\. To help provide an example, type the following into the Python Console, and press enter to execute the command\.



```python
>>> "1" * 2
'11'
```



Now it works like a charm\. Not only did the command contain the data type "str", and also an "int" as it expected\. Another way of saying this is that the command provided correct Python Syntax\. Type the following into the Python Console, and then press enter to execute the command:



```python
>>> "you are a python wizard"[0]
'y'
```



The command included a string, and then "\[0\]"\. The command, in english, means output the first letter in the string, which in this case, is "y"\. Though it would be easier to understand the number if it was one, it is 0 because it represents 'first'\. Note that a character doesn't have to be a letter\. It can be "\!", "@", "4", or of course any mix of that\.



###3\.  Text editor

The Python interpreter prompt is really fun and useful, but scripts and addons rarely are one line long\. That being said, something is required that will allow the typing and execution of multiple lines as one script\. Luckily, the only thing that's necessary is a regular text file with \*\.py extension\. This is called a Python module\. In order to edit a Python module, a text editor is necessary\. The preferred choice is an editor that can highlight Python syntax, which means that it colors differently different Python commands to make them easier to notice\. Python already comes with a text editor bundled with a GUI python interpreter prompt called IDLE , that it works very good for Python coding\. So you can use IDEL to create python modules \. To execute python modules all you have to do in the terminal is :



```python
python mymodule.py
```



of course you replace "mymodule\.py" with the name of your module\. If you decide to use IDLE then you can bypass the terminal completely and instead use IDLE's "run module" option you can find in its menu bar\.
