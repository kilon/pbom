

##Variables



###1\. Assignment

OK, let's get back to coding\. Where were we? Ah, yes\. We explained data types such as integers and strings\. But would it be cool if we could store data in some way, after your computer already stored data in files on a hard disk, on memory, online, etc\. Data changes all the time, so storage is a must\.

Programming languages store data in variables\. Let's see this example\.



```python
a = 12
b = "I have"
c = "ideas"
print(b+" "+str(a)+" "+c)
```



OK, let's take this step by step\. On the first line, we define a variable called “a”, and we store inside it the 12, an int value\. Assigning variables is that easy\. You basically provide the name, equal sign, and a value\. On the second line, we define a variable called “b”, stored inside "I have", a str value\. Last but not least, the third line defines “c”, is assigned "ideas", another str value\.

The next line takes a bit of explaining, but is easy to figure it out\. It's a print function\. It's a function because it has a name, a parameter, and opening and closing parentheses\. The "\+" is used as an operator to unite the strings\. A variable can be of any type, but as I said, Python does not like it when you mix different types because our print function only takes string values\. If we just let it be "\+a", it would complain with an error because it is an integer \(int value\)\. What we need to do is convert variable "a"'s value to a string\. Since we can use int\(\) and float\(\) to convert a type to an integer or float, we should be able to convert a type to a string by using str\(\)\. Therefore, the function str\(\) is used with the parameter “a”\.

Notice that we used \+" " as part of the parameter of the print function to type spaces between the strings\. We could have as well included those spaces in the strings when we assigned the variables\. The beauty of coding is that it allows us to be flexible\.



###2\.  User input

A program that does not interact with a user is not a very useful program\. What if we could communicate with the user in some way? We can, using the input\(\) function\.



```python
name = input("What's your name?")
print("Hello "+name+". My name is Python, nice to meet you." )
```



Go ahead and type your name and hit enter\. If you typed John, it will print "Hello John\. My name is Python, nice to meet you"\. Isn't Python fun?\!


As you can see, we assign the output of the function input\(\) to a variable\. Functions can take input with parameters and can output data with returning types\. In this case, it returns data type 'str', and to be precise, a string with the name we input\. From there on we just unite the name variable with the 2 other strings to form the final print\.

Let's try the following code:



```python
number1 = int(input("Give me the first number : "))
number2 = int(input("Give me the second number : "))
print( "If I add " + str(number1) + " and "+str(number2)+" it equals to "+str(number1+number2))
```



Don't let this confuse you; it's still easy to understand\. The first thing you observe is that it is possible for a function to take another function as a parameter\. What we did in line 1 and 2 is that we take input from the user and convert it into integer, remembering that input returns only strings\. Then in the print function, we reconvert the variables to strings in order to unite them in one string\. After that, we add variable number1 and number2 together\. The result is converted to a string, which is then united to the final string\.

There is another way of doing this, shown below:



```python
number1 = input("Give me the first number : ")
number2 = input("Give me the second number : ")
print( "If I add %s and %s it equals to %d"  %(number1 ,number2, int(number1)+int(number2)))
```



So this is doing the exact same thing, it only does it differently\. The "%s" inside our string is not actually part of string\. It only tells print that it should place a string here, which is defined inside %\(\)\. So the first %s places the string value of number1 the second %s places the string value of number2\. However, %d places an integer which is the the result of converting number1 variable and number2 variable to integers and then adding them together\. As you see, with this way we don't have to convert our variables except only when we add them together\. This process is called string formatting\. It is useful for when you do many conversions between different types and want to join everything in a single string\. What you use is up to you\.



###3\.  Variable rules

There are some rules to be followed for variables\. First, when you name them, you are allowed to use numbers inside but the name of the variable must start with a letter\. Below is what NOT to do:



```python
123 = 3
```



Do not do this either:



```python
123b = 3
```



Don't put spaces in variable names:



```python
number 1= 3
```



You can do this though:



```python
number_1= 3
```



You also can do this, because it's possible to give a variable a different value at any time:



```python
number_1= 3
number_1 = 4
```



Variables can also be assigned values contained in other variables\. The final value of the variable in this case will be 4\.



```python
number_1= 3
number_2 = 4
number_1 = number_2
```



However, if we do this, again the final value of number\_1 will be 4\. Why is this? Because the variable change of number\_2 doesn't change the value of number\_1 after assignment\.



```python
number_1= 3
number_2 = 4
number_1 = number_2
number_2 =10
```





###4\. 3\.4 Case Sensitivity

Another extremely important rule that applies to everything in Python is case sensitivity\. Case sensitivity is the capitalization of letters\. For example, Var1 and var1 are two different variables\. That means that capitalization matters A LOT\. Many programmers use it for naming\. MyFirstVariable is, of course, different from myfirstvariable or mYfirsTvariable, etc\. Personally, I don't use capitalization to name anything I define or assign\. I prefer the use of underscores, but it's completely up to you\. Bare in mind that capitalization applies to everything inside Python, so you need to be careful how you type your commands\.
