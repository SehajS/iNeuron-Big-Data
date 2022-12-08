
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


Q26. What is a string? How can we declare string in Python?

A26. A string is a sequence of characters. It is declared by enclosing the characters in either single quotes, double quotes as shown below:
``` {python}
my_str = "abcd"
```

Q27. How can we access the string using its index?

A27. In a similar manner as accessing an element at an index i for a list. Say you have a string `my_str`, then ith element of that string can be accessed using `my_str[i-1]`.

Q28. Write a code to get the desired output of the following
```
string = "Big Data iNeuron"
desired_output = "iNeuron"
```
A28. 
```{python}
desired_output = string[-7:]
```

Q29. Write a code to get the desired output of the following
```
string = "Big Data iNeuron"
desired_output = "norueNi"
```

A29.
```{python}
"".join(string.split(" ")[-1][::-1])
```

Q30. Resverse the string given in the above question.

A30.
```{python}
string[::-1]
```

Q31. How can you delete entire string at once?

A31. One can use the `del` keyword to delete an entire string as shown below:

```
del mystr
```

Q32. What is escape sequence?

A32. A sequence of characters that when used inside a string are converted to another character or series of characters. For example, `\n` is a sequence character to indicatea new line in the string. 

Q33. How can you print the below string?
```
'iNeuron's Big Data Course'
```
A33.  Use double quotes as opposed to single quotes
```{python}
print("'iNeuron's Big Data Course'")
```

Q34. What is a list in Python?

A34. List is a data structure that allows for storing muliple values. It is basically a sequence that is accessed using only one  variable. 

Q35. How can you create a list in Python?

A35. Lists are created using square brackets as shown below:

```
courses = ['Data Science', 'Big Data', 'Data Analytics', 'Machine Learning']
```

Q36. How can we access the elements in a list?

A36.  The elements in the list are accessed by utilizing square brackets and passing the index of the element as shown below:

```
list_a = ['big data','power bi', 'machine learning']
# to access 2nd element of the list one would use the following
print(list_a[1])
```

Q37. Write a code to access the word "iNeuron" from the given list.
```
lst = [1,2,3,"Hi",[45,54, "iNeuron"], "Big Data"]
``` 
A37.
```{python}
lst[-2][-1]
```

Q38. Take a list as an input from the user and find the length of the list.

Q39. Add the word "Big" in the 3rd index of the given list.
```
lst = ["Welcome", "to", "Data", "course"]
```
A39.
```{python}
lst.insert(3, "Big")
```

Q40. What is a tuple? How is it different from list?
```
A tuple is data structure that allows for storage of multiple items. In contrast to lists, tuples are immutable.
```

Q41. How can you create a tuple in Python?

A41. Tuples are created using parathesis like the one below:

```
courses = ('Data Science', 'Big Data', 'Data Analytics', 'Machine Learning')
```

Q42. Create a tuple and try to add your name in the tuple. Are you able to do it? Support your answer with reason.

A42. It would not work since tuples are immuatable - i.e., once created, they cannot be changed.

Q43. Can two tuple be appended. If yes, write a code for it. If not, why?

A43. Yes, two tuples can be appended to create a new tuple as shown below:
```
tup_1 = (1, 2)
tup_2 = (2, 3)
print(tup_1 + tup_2) # results in (1, 2, 2, 3)
```

Q44. Take a tuple as an input and print the count of elements in it.

```{python}
from collections import Counter
def get_counts(tuple_a):
	return Counter(tuple_a)
```

Q45. What are sets in Python?

A45. A data structure that allows for storing multiple unordered unique items.

Q46. How can you create a set?

A46. A set is created using curly braces as shown below:

```{python}
set_a = {'Data Science', 'Big Data', 'Data Analytics', 'Machine Learning'}
```

Q47. Create a set and add "iNeuron" in your set.
```{python}
set_a = {}
set_a.add("iNeuron")
```
Q48. Try to add multiple values using add() function.

Q49. How is update() different from add()?

Q50. What is clear() in sets?

A50. It turns a set into an empty set by removing all its elements.

Q51. What is frozen set?

Q52. How is frozen set different from set?

Q53. What is union() in sets? Explain via code.

A53. It creates a new set which contains all the elements of both the sets on which union is applied to. 

```{python}
set_a  = {1, 2, 3}
set_b = {3, 5, 6}

union_set = set_a.union(set_b)
print(union_set)
# {1, 2, 3, 5, 6}
```

Q54. What is intersection() in sets? Explain via code.

A54. It creates a new set which contains only those elements that are present in both the sets.

```{python}
set_a  = {1, 2, 3}
set_b = {3, 5, 6}

intersection_set = set_a.intersection(set_b)
print(intersection_set )
# {3}
```

Q55. What is dictionary in Python?

A55. A data structure that allows for storing key value pairs. Instead of indices as in the case with lists, keys are used to access the values in a dictionary.

Q56. How is dictionary different from all other data structures.

Q57. How can we delare a dictionary in Python?

Q58. What will the output of the following?
```
var = {}
print(type(var))
```

A58.  The output will be `<class 'dict'>`.

Q59. How can we add an element in a dictionary?

A59. An element can be added in the dictionary by simply using square brackets as shown below:

```{python}
sample_dict = {'a':1, 'b':2, 'c':3}
sample_dict['d'] = 4 # new element 'd' added
```

Q60. Create a dictionary and access all the values in that dictionary.

A60.
```{python}
sample_dict = {'a':1, 'b':2, 'c':3}
for key, val in sample_dict.items():
	print(key, val)
```

Q61. Create a nested dictionary and access all the element in the inner dictionary.

A61.
```{python}
sample_dict = {'a':1, 'b':2, 'c': {'c1': 3, 'c2': 4}}
for key, val in sample_dict['c'].items():
	print(key, val)
```

Q62. What is the use of get() function?

A62. It is used to access the corresponding value of a key in the dictionary. Sample code is shown below:

```{python}
sample_dict = {'a':1, 'b':2, 'c': {'c1': 3, 'c2': 4}}
print(sample_dict.get('a')) # will print 1
```

Q63. What is the use of items() function?

Q64. What is the use of pop() function?

Q65. What is the use of popitems() function?

Q66. What is the use of keys() function?

Q67. What is the use of values() function?

Q68. What are loops in Python?

Q69. How many type of loop are there in Python?

Q70. What is the difference between for and while loops?

Q71. What is the use of continue statement?

Q72. What is the use of break statement?

A72. The break statement allows for stopping execution of a loop if a particular condition is met.

Q73. What is the use of pass statement?

Q74. What is the use of range() function?

Q75. How can you loop over a dictionary?


### Coding problems
Q76. Write a Python program to find the factorial of a given number.

```{python}
def factorial(n):
	if n == 0 or n == 1:
		return n
	result = 1
	for i in range(2, n+1):
		result *= i
	return result
```

Q77. Write a Python program to calculate the simple interest. Formula to calculate simple interest is SI = (P*R*T)/100

```{python}
def si(p,r,t):
	return (p*r*t)/100
```

Q78. Write a Python program to calculate the compound interest. Formula of compound interest is A = P(1+ R/100)^t.
```{python}
def compound_interest(p, r,t):
	return p*(1+r/100)**t
```
Q79. Write a Python program to check if a number is prime or not.
```{python}
import math
def check_prime(n):
	for i in range(1, math.floor(math.sqrt(n)):
		if n%i == 0:
			return "Prime"
	return "Not Prime"
```
Q80. Write a Python program to check Armstrong Number.
```{python}
def check_armstrong(num):
	sum_of_cubes = 0
	for i in str(num):
		sum_of_cubes += int(i)**3
	return sum_of_cubes == num
```

Q81. Write a Python program to find the n-th Fibonacci Number.
```{python}
def fib(n):
	if n == 0 or n == 1:
		return 1
	fib_list = [1, 1]
	for i in range(2, n+1):
		fib_list.append(fib_list[-1] + fib_list[-2])
	return fib_list[-1]
```
Q82. Write a Python program to interchange the first and last element in a list.
```{python}
def interchange(list_a):
	list_a[0], list_a[-1] = list_a[-1], list_a[0]
	return list_a
```
Q83. Write a Python program to swap two elements in a list.
```
def swap(list_a, x, y):
""" x and y are the elements of list_a that are to be swaped """
	index_1 = list_a.index(x)
	index_2 = list_a.index(y)
	list_a[index_1] = y
	list_a[index_2] = x
	return list_a
```
Q84. Write a Python program to find N largest element from a list.
```{python}
def largest_n(list_a, n):
    list_b = sorted(list_a)[::-1]
    return list_b[n-1]
```

Q85. Write a Python program to find cumulative sum of a list.

```{python}
def get_cummulative(list_a):
    return [list_a[i] + sum(list_a[0:i]) for i in range(len(list_a))]
```

Q86. Write a Python program to check if a string is palindrome or not.

```{python}
def check_palindrome(my_str):
	reversed = my_str[::-1]
	return my_str == reversed
```

Q87. Write a Python program to remove i'th element from a string.
```{python}
def remove_ith(my_str, i):
""" i must be greater than 0 """
	return my_str[:i-1] + my_str[i:]
```

Q88. Write a Python program to check if a substring is present in a given string.

```{python}
def check_substring(sub, my_str):
	return sub_ in my_str
```

Q89. Write a Python program to find words which are greater than given length k.
```{python}
def check_length(word, k):
	return len(word) > k
```

Q90. Write a Python program to extract unquire dictionary values.
```{python}
from itertools import chain
def get_unique_values(dict_1):
	vals = [val for key, val in dict_1.items()]
	chained = chain(*vals)
	return set(chained)
```

Q91. Write a Python program to merge two dictionary.
```{python}
def merge_dicts(dict_1, dict_2):
	return {**dict_1, **dict_2}
```

Q92. Write a Python program to convert a list of tuples into dictionary.
```
Input : [('Sachin', 10), ('MSD', 7), ('Kohli', 18), ('Rohit', 45)]
Output : {'Sachin': 10, 'MSD': 7, 'Kohli': 18, 'Rohit': 45}
```
```{python}
def tuple2dict(list_a):
	return dict(list_a)
```
Q93. Write a Python program to create a list of tuples from given list having number and its cube in each tuple.
```
Input: list = [9, 5, 6]
Output: [(9, 729), (5, 125), (6, 216)]
```
```{python}
def get_tuples(list_a):
	return [(i, i**3) for i in list_a]
```

Q94. Write a Python program to get all combinations of 2 tuples.
```
Input : test_tuple1 = (7, 2), test_tuple2 = (7, 8)
Output : [(7, 7), (7, 8), (2, 7), (2, 8), (7, 7), (7, 2), (8, 7), (8, 2)]
```
```{python}
def tuple_combinations(tuple_1, tuple_2):
	result = [(i, j) for i in tuple_1 for j in tuple_2]
	reverse = [(j, i) for i in tuple_1 for j in tuple_2]
	return result + reverse
```

Q95. Write a Python program to sort a list of tuples by second item.
```
Input : [('for', 24), ('Geeks', 8), ('Geeks', 30)] 
Output : [('Geeks', 8), ('for', 24), ('Geeks', 30)]
```
```{python}
def sort_list_of_tuples(list_a):
	list_a.sort(key = lambda x: x[1])
	return list_a
```

Q96. Write a python program to print below pattern.
```
* 
* * 
* * * 
* * * * 
* * * * * 
```

```{python}
for i in range(1, 6):
	print("* " * i)

```

Q97. Write a python program to print below pattern.
```
    *
   **
  ***
 ****
*****
```
```{python}
for i in range(1, 6):
	result = " " * (5-i)
	result += "*" * i
	print(result)
```

Q98. Write a python program to print below pattern.
```
    * 
   * * 
  * * * 
 * * * * 
* * * * * 
```

```{python}
for i in range(1, 6):
	print(" " * (5-i) + "* " * i)	
```

Q99. Write a python program to print below pattern.
```
1 
1 2 
1 2 3 
1 2 3 4 
1 2 3 4 5
```
```{python}
for i in range(1, 6):
	print(*range(1, i+1))
```
Q100. Write a python program to print below pattern.
```
A 
B B 
C C C 
D D D D 
E E E E E 
```
```{python}
characters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
for i in range(1, 6):
	print((characters[i-1] + " ") *  i)
```