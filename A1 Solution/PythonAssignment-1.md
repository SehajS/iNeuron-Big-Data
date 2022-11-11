
## Assignment Part-1

Q1. Why do we call Python as a general purpose and high-level programming language?

A1. Python is a general purpose programming language, i.e., it is used to build wide variety of applications in multiple domains - it can be used in back-end development, can be used in data analysis, machine learning, etc. This is opposite of a specific purpose language, for example SQL which is used only to query/interact with databases. Python is also a high-level programming language in the sense that one does not have to directly write up machine language to run programs which is the case with low-level languages like assembly languages. Python utilizes an abstraction from high level language, and a compiler is used to convert the human-readable code to machine language.

<br>
Q2. Why is Python called a dynamically typed language?

A2. A dynamically typed language is one where one doesn't need to explicitly mention the datatype of the variable while creating it. The language's interpreter will assign the datatype to the variable during runtime based on the value stored in the variable. Since Python has this property, it is thus called a dynamically typed language.
  
<br>
Q3. List some pros and cons of Python programming language?

A3. Some pros of Python are as follows:
- It is more human readable as compared to other programming languages.
- It is easier to learn because of ease of syntax.
- The programs written in Python are easier to debug.
- One can build applications in multiple domains - machine learning, web development, data analysis, automation, etc.

Some of the cons of Python are as follows:
- It is slower as compared to other object oriented languages like C++ and Java.

<br> 
Q4. In what all domains can we use Python?

A4. Python can be used in data science, data engineering, data analytics, automation, application development as well as in building some basic games too. There are many other use cases of Python as well but the above ones are the most popular uses.
<br>
Q5. What are variable and how can we declare them?

A5. A variable is a symbolic name that is used to store data values. Declaring of a variable can be done using assignment operator `=` like in the following example where variable `a` is assigned the value of 5. 
```
a = 5
```
<br>
Q6. How can we take an input from the user in Python?

A6. One can get input from the user by using the Python's built-in `input()` function. For example, in order to get name of the user, one can do the following:

```{python}
name = input("Enter your name: ")
```

<br>
Q7. What is the default datatype of the value that has been taken as an input using input() function?

A7. The default type for input() function is string.
<br> 
Q8. What is type casting?

A8. Type casting means converting a variable or a data point from one datatype to another. Below is an example to do that:
```{python}
a = 4 # this is an integer
b = str(a) # converts a into string dtype - this is typecasting
```
<br>
Q9. Can we take more than one input from the user using single input() function? If yes, how? If no, why?

A9. Yes, one can take more than one input from the user using single input() function. One way to do that is utilizing `split()` function along with a list comprehension as shown below:
```{python}
# taking multiple values
nums = [int(x) for x in input("Enter multiple values: ").split()]
```
Resource: https://www.geeksforgeeks.org/taking-multiple-inputs-from-user-in-python/

<br>
Q10. What are keywords?

A10. Keywords are certain reserved words that have a very specific use in Python and cannot be used for any other purposes. Some examples of such keywords are if, else, elif, class, def, while, for, etc.
 
 <br>
Q11. Can we use keywords as a variable? Support your answer with reason.

A11. No, one can never use keywords as variable names. This is because `SyntaxError` will be thrown if one tries to do that. Keywords have a very specific use in Python and assigning a value to them is by design not allowed by Python - it can otherwise lead to confusion while reading the code as well as can lead a pathway to some serious problems that will be harder to debug. 

<br>
Q12. What is indentation? What's the use of indentaion in Python?

A12. Indentation refers to spaces at the beginning of a code line. Indentation is used to represent a particular block of code. For example, everything that to be executed after an `if` condition is true, should be indented right after the if statement. Every statement that is not indented after the `if` statement is not part of the code block for that `if` statement. 
  
<br>
Q13. How can we throw some output in Python?

A13. One can use the `print()` function to throw output. Anything inside that print clause is displayed on the IDE.
<br>
Q14. What are operators in Python?

A14. Operators are some special symbols that allow for execution of mathematical as well as non-mathematical operations to be performed depending upon the data points they are applied to. Some common operators are +, -, /, //, *, %, etc.
For example:
```{python}
print(4 + 5) # gives us 9 where it is normal integer addition
print([1, 2] + [3, 4]) # gives [1, 2, 3, 4]
```
<br>
Q15. What is difference between / and // operators?

  A15. The operator / performs normal division and will give a float as a result while the // operator will discard every digit across decimal point and will return only the integer quotient as the result. For example: 5/2 will result in 2.5 while 5/2 will result in 2.
<br>
Q16. Write a code that gives following as an output.

```
iNeuroniNeuroniNeuroniNeuron
```
A16.
```{python}
x = "iNeuron"
print(x*4)
```
  
<br>
Q17. Write a code to take a number as an input from the user and check if the number is odd or even.

A17.
```{python}
x = int(input("Enter a number: "))
if x%2 == 0:
	print(f"{x} is even")
else:
	print(f"{x} is odd")
```
  <br>

Q18. What are boolean operator?

A18. The operators `and`, `or` and `not` are referred to as boolean opeartors in Python - they perform logical operations to give out the truth value (`True` or `False` boolean dataype) for an expression.
<br>  
Q19. What will the output of the following?

```

1 or 0

  

0 and 0

  

True and False and True

  

1 or 0 or 0

```

A19.
```
1 or 0 ->True
0 and 0 -> False 
True and False and True -> False
1 or 0 or 0 -> True
```
<br>
Q20. What are conditional statements in Python?

A20.  Conditional statements are decision-making statements in the sense that if a certain condition is satisfied only then the block of code associated with that condition is executed. Some examples of conditional statements are if, elif, else, switch-case and match-case.

<br>
Q21. What is use of 'if', 'elif' and 'else' keywords?

A21. They allow execution of a certain block of code depending upon which condition is being met. For example, say if we want to check whether a number is zero, positive or negative. Then, one can write up the following code:
```{python}
def check_num(x):
	if x == 0:
		print("Number is zero")
	elif x >= 0:
		print("Number is positive")
	else:
		print("Number is negative")
```
Only that print statement will be executed whose condition is satisfied by the parameter x.
 <br>

Q22. Write a code to take the age of person as an input and if age >= 18 display "I can vote". If age is < 18 display "I can't vote".

A22.
```{python}
age = int(input("Enter your age: "))
if age >= 18:
	print("I can vote")
else:
	print("I can't vote")
```
  <br>

Q23. Write a code that displays the sum of all the even numbers from the given list.

```

numbers = [12, 75, 150, 180, 145, 525, 50]

```
A23.

```{python}
numbers = [12, 75, 150, 180, 145, 525, 50]
evens = [num for num in numbers if num%2 == 0]
print(sum(evens))
``` 
<br> 

Q24. Write a code to take 3 numbers as an input from the user and display the greatest no as output.

A24.

```{python}
x = float(input("Enter the first number: "))
y = float(input("Enter the second number: "))
z = float(input("Enter the third number: "))

print(f"The greatest of the three numbers is {max(x, y, z)}")
```
  

Q25. Write a program to display only those numbers from a list that satisfy the following conditions

  

- The number must be divisible by five

  

- If the number is greater than 150, then skip it and move to the next number

  

- If the number is greater than 500, then stop the loop

```

numbers = [12, 75, 150, 180, 145, 525, 50]

```

A25.
```{python}
numbers = [12, 75, 150, 180, 145, 525, 50]
divisible_by_5 = [num for num in numbers if num%5 ==0]
i = 0
while i < len(divisible_by_5):
	if divisible_by_5[i] > 500:
		break
	if divisible_by_5[i] > 150:
		pass
	else:
		print(divisible_by_5[i])
	i += 1
```