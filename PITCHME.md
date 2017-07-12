

## Sheriff Adeoti
<br>
<span style="color:#536DFE">Python</span>
<br>
<span style="color:#536DFE">Training</span>

---

### Python Introduction

## Python Keywords
<br>
Keywords are the reserved words in Python.
We cannot use a keyword as variable name, function name or any other identifier. They 

are used to define the syntax and structure of the Python language.

In Python, keywords are case sensitive.

There are 33 keywords in Python 3.3. This number can vary slightly in course of time.

All the keywords except True, False and None are in lowercase and they must be written 

as it is. The list of all the keywords are given below.

---
## Keywords in Python programming language

<br>_
| False | class	| finally | is	|return |
|------|--------|---------|-----|-------|
| None	| continue | for | lambda | try |
|True | def | from | nonlocal | while |
| and | del | global | not | with |
| as | elif | if | or |	yield |
| assert | else	| import | pass |
| break	| except | in | rais |
 <br>
Looking at all the keywords at once and trying to figure out what they mean might be 

overwhelming.

---

### Python Identifiers

<br>
Identifier is the name given to entities like class, functions, variables etc. in 

Python. It helps differentiating one entity from another.

## Rules for writting Identifiers

<ol>
<ol>Identifiers can be a combination of letters in lowercase (a to z) or uppercase (A to 

Z) or digits (0 to 9) or an underscore (_). Names like myClass, var_1 and 

print_this_to_screen, all are valid example.</ol>
<ol>An identifier cannot start with a digit. 1variable is invalid, but variable1 is 

perfectly fine.</ol>
<ol>Keywords cannot be used as identifiers.</ol>

```python
>>> global = 1
  File "<interactive input>", line 1
    global = 1
           ^
SyntaxError: invalid syntax
```
<ol>
<ol>We cannot use special symbols like !, @, #, $, % etc. in our identifier.</ol>
---

```python
>>> a@ = 0
  File "<interactive input>", line 1
    a@ = 0
     ^
SyntaxError: invalid syntax
```
<ol>Identifier can be of any length.</ol>

---
#### Things to care about
<br>
Python is a case-sensitive language. This means, Variable and variable are not the same. 

Always name identifiers that make sense.

<br>
While, c = 10 is valid. Writing count = 10 would make more sense and it would be easier 

to figure out what it does even when you look at your code after a long gap.
Multiple words can be separated using an underscore, this_is_a_long_variable.
---

<br>
We can also use camel-case style of writing, i.e., capitalize every first letter of the 

word except the initial word without any spaces. For example: camelCaseExample

---
## Python Statement, Indentation and Comments

#### Python Statement

<br>
Instructions that a Python interpreter can execute are called statements. For example, a 

= 1 is an assignment statement. if statement, for statement, while statement etc. are 

other kinds of statements which will be discussed later.

#### Multi-line statement

<br>
In Python, end of a statement is marked by a newline character. But we can make a 

statement extend over multiple lines with the line continuation character (\). For 

example:


```python
a = 1 + 2 + 3 + \
    4 + 5 + 6 + \
    7 + 8 + 9
```
---
<br>
This is explicit line continuation. In Python, line continuation is implied inside 

parentheses ( ), brackets [ ] and braces { }. For instance, we can implement the above 

multi-line statement as

```pyhton
a = (1 + 2 + 3 +
    4 + 5 + 6 +
    7 + 8 + 9)
```
<br>
Here, the surrounding parentheses ( ) do the line continuation implicitly. Same is the 

case with [ ] and { }. For example:
 
```python
colors = ['red',
          'blue',
          'green']
```
<br>
We could also put multiple statements in a single line using semicolons, as follows

```python
a = 1; b = 2; c = 3
```
---

#### Python Indentation

<br>
Most of the programming languages like C, C++, Java use braces { } to define a block of 

code. Python uses indentation.

<br>
A code block (body of a function, loop etc.) starts with indentation and ends with the 

first unindented line. The amount of indentation is up to you, but it must be consistent 

throughout that block.
---

Generally four whitespaces are used for indentation and is preferred over tabs. Here is 

an example.

```python
for i in range(1,11):
	print(i)
	if i == 5:
		break
```

The enforcement of indentation in Python makes the code look neat and clean. This 

results into Python programs that look similar and consistent.

<br>
Indentation can be ignored in line continuation. But it's a good idea to always indent. 

It makes the code more readable. For example:

```python
if True:
    print('Hello')
    a = 5
```
and
---
```python
if True: print('Hello'); a = 5
```
<br>
both are valid and do the same thing. But the former style is clearer.

Incorrect indentation will result into IndentationError

---
#### Python Comments
<br>
Comments are very important while writing a program. It describes what's going on inside 

a program so that a person looking at the source code does not have a hard time figuring 

it out. You might forget the key details of the program you just wrote in a month's 

time. So taking time to explain these concepts in form of comments is always fruitful.
---

In Python, we use the hash (#) symbol to start writing a comment.
<br>
It extends up to the newline character. Comments are for programmers for better 

understanding of a program. Python Interpreter ignores comment.

```python
#This is a comment
#print out Hello
print('Hello')
```
---
#### Multi-line comments

<br>
If we have comments that extend multiple lines, one way of doing it is to use hash (#) 

in the beginning of each line. For example:

```python
#This is a long comment
#and it extends
#to multiple lines
```
---

Another way of doing this is to use triple quotes, either ''' or """.

These triple quotes are generally used for multi-line strings. But they can be used as 

multi-line comment as well. Unless they are not docstrings, they do not generate any 

extra code.

```python
"""This is also a
perfect example of
multi-line comments"""
```
---

#### Docstring in Python
<br>
Docstring is short for documentation string.

It is a string that occurs as the first statement in a module, function, class, or 

method definition. We must write what a function/class does in the docstring.

Triple quotes are used while writing docstrings. for example

```python
def doublele(num):
	"""Function to double the value"""
	return 2*num
```
---
<br>
Docstring is available to us as the attribute __doc__ of the function. Issue the 

following code in shell once you run the above program.

```python
>>> print(double.__doc__)
Function to double the value
```
