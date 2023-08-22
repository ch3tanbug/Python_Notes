# Python_Notes
All the notes i made while learning python

## Modules
REPL - Read Evaluate Print Loop

Modules help us to borrow code written by other developers.
There are two types of modules -
1. Built in Modules - These are installed/shipped with the python language itself
2. External Modules - Written by other people we dont generally know their implementation we are only concerned about its interface

## PIP Command
It is basically a package manager which can be used to install a python module
command -
```
pip install pandas (in linux and mac it may require pip3)
```

## Using a Module
We use `#include` modulename to import any module in python
Example-
        `import pandas`

## Print()
Print() is a function in python that displays content out to screen. Print reqquires an object to be passed but we 
can also specify string by using  `""`

Example-
```python
print("Hello World")
```

Print() also accepts multiple arguments and prints each argument followed by a space
```python
print("Chetan",30)
```
We can also do computations in print() itself
```python
print(7*7)
```

## Comments, Escape sequences & print statement
comments are the part of the code that the programmer doesnt want to be executed rather it is used to explain a block of code or functionality.
```python
 #yourcomment (single line comment)
"""anything
anything"""  (multi-line comment)
```
    
To insert characters that cannot be directly used in a string we use Escape sequence characters. It is a backslash(\) followed by the character.

Example-
```python
print("Hello \n chetan")
print("\"good developer\"")
```
    
### Parameters of print statement
1.`sep` = used to join the various given agruments with any symbol specified
```python
        print("chetan",7,sep="~")
```
2.`end` = will print given value before the next used print statement or when the current print ends
```python
        print("chetan",30,end="end begins")
```
3.`file` = An object with a write method. Default is sys.stdout

## Variables and Datatypes
Variable is just like a container that can hold any type of data. Creating a variable is just like creating a placeholder
in memory and assigning it a value.
```python
a = 1
b = True   #this is boolean
c = "Harry"
d = None
```
    
Data type specifies the type of value a variable holds. This is required in programming to do various operations without causing an error.

If we want to know the datatype of a given variable we can use type(variablename) in python

### Types of datatypes-

1. `Numeric data`: int, float, complex
    1. `int`: 3, -8, 0
    2. `float`: 7.349, -9.0, 0.0000001
    3. `complex`: 6 + 2i    # to create complex number in python use complex(realno,imaginaryno)
        
2. `Text data`: str
    1. `str`: "Hello World!!!", "Python Programming"
        
3.`Boolean data`:

Boolean data consists of values True or False.
        
4.`Sequenced data`: list, tuple

`list`: A list is an ordered collection of data with elements separated by a comma and enclosed within square brackets. Lists are mutable and can be modified after creation.
```python
list1 = [8, 2.3, [-4, 5], ["apple", "banana"]]
print(list1)
```
            
5. `Tuple`: A tuple is an ordered collection of data with elements separated by a comma and enclosed within parentheses. Tuples are immutable and can not be modified after creation.
```python
tuple1 = (("parrot", "sparrow"), ("Lion", "Tiger"))
print(tuple1)
```
        
6.`Mapped data`: dict

`dict`: A dictionary is an unordered collection of data containing a key:value pair. The key:value pairs are enclosed within curly brackets.
```python
dict1 = {"name":"Sakshi", "age":20, "canVote":True}
print(dict1)
```

# Operators
Operators are symbols in python used to perform some specific operation

Types of builtin operators-
1. `+`   -   add
2. `-`   -   subtraction
3. `*`   -   multiplication
4. `**`  -   exponential
5. `/`  -   division (returns quotient)
6. `%`  -   modulus (returns remainder)
7. `//`  -   floor division (returns quotient as whole number)

# Typecasting in Python
The conversion of one datatype into another datatype is what we refer to as Typecasting

Python supports plenty of functions for performing typecasting like int(), float(), str(), ord(), hex(), oct(), tuple(), set(), list(), dict(), etc

There are two type of typecasting -

1. `Explicit Conversion (Explicit type casting in python)` - This is done by the programmer manually as per requirement it is achieved by using functions like int(),float() etc.
```python
            a="9"
            b="7"
            print(a+b) # this will show 97 as output
            print(int(a)+int(b)) # this will show 16 as output because of type casting
```

2. `Implicit Conversion (Implicit type casting in python)` -   Datatypes in python do not have same order. So when an operation is performed between two different datatypes the python interpreter automatically converts the smaller datatype to the higher datatype to prevent data loss this is called implicit conversion or typecasting.
```python
        a=9.9
        b=7
        print(a+b)  # this will show 16.9 as output because of implicit type casting
```

# Taking user input in python
We can taker user input in python with the help of input() function. It generally returns value as string or character.
But input function returns the value as string. Hence we have to typecast them whenever required to another datatype.
We can also display a text using input function. This will make input() function take user input and display a message as well.
```python
        a=int(input("Enter a number: "))  #typecasting as int() in input as well as displaying message
```

# Strings
In python, anything that you enclose between single or double quotation marks is considered a string. A string is essentially a sequence or array of textual data. Strings are used when working with Unicode characters.

`eg- "Chetan"`

It doesnt matter if you use single quotation marks or double quotation marks while making a string.
If you want to use `(" or ')` inside a string you can use escape sequence characters like `/"` or `/'` or you can enclose single quotation marks inside double quotationmark string and vice versa
```python
eg - print("hello 'chetan'") or print ("hello /'chetan/'")
```

### Multiline Strings
If our string has multiple lines it can be created like -
```python
''' hello
chetan
how are
you'''
```
    
## Acessing Individual elements of string
In python a string is not exactly an array of characters but is somewhat like that. We can access it characters with the help of indexes which start from 0.

eg -
```python
print(stringvariable[0]) #here 0 is an index
```
    
### Looping through a string
We can also loop though a string and print its every individual character seperately with the help of a for loop.
```python
for character in a:
  print(character)
```
    
### String Slicing & Operations on Strings
Length of a string can be identified using the len function
```python
print(len(strng))
```
    
Note: Always use () for functions and [] for slicing 

### String as an array
A string is somewhat like an array of characters therfore we can access the elements. 

eg - 
```python
print(name[0:4]) #It will only print first 3 elements 4 element will not be printed
print(name[:4])  # same as above python automatically inserts 0
```
                
### Negative Slicing
`print(name[0:-3])` this is same as `print(name[0:len(name)-3])` which means if name len is 5 it will be like `print(name[0:2])`
    
##String Methods
strings are immutable therefore whenever we invoke a string method we get a copy of original string
 1. `upper()` - Converts string to uppercase
```python
                print("string".upper())
```
2. `lower()` - Converts string to lowercase
```python
                print("string".lower())
```
3. `strip()` - The strip() method removes any white spaces before and after the string.
```python
                print(" hello ".strip())
```
4. `rstrip()` - the rstrip() removes any trailing characters.
```python
                print("hello!!!".rstrip("!"))
```
5. `replace()` - The replace() method replaces all occurences of a string with another string.
```python
                print(str.replace("ch","mh")) # finds occurances of ch and replaces with mh
```
6. `split()` - The split() method splits the given string (basically converts string to list) at the specified instance and returns the separated strings as list items.
```python
                print(str.split(" ")) #splits the string at whitespaces
```
7. `capitalize()` - The capitalize() method turns only the first character of the string to uppercase and the rest other characters of the string are turned to lowercase. The string has no effect if the first character is already uppercase.
```python
                print("hello".capitalize())
```
8. `center()` - The center() method aligns the string to the center as per the parameters given by the user.
```python
                print("hello".center(50)) #this 50 contains length of string itself also
                We can also provide padding character. It will fill the rest of the fill characters provided by the user.
                print("hello".center(50,"."))    #will display in center like .....hello.....
```
9. `count()` - The count() method returns the number of times the given value has occurred within the given string.
```python
                print("hello".count("l"))
```
10. `endswith()` - The endswith() method checks if the string ends with a given value. If yes then return True, else return False.
```python
print("hello".endswith("o"))
# We can even also check for a value in-between the string by providing start and end index positions.
print("hello".endswith("o",0,5))
```
11. `find()` - The find() method searches for the first occurrence of the given value and returns the index where it is present. If given value is absent from the string then return -1.
```python
                print("hello".find("e"))
```
As we can see, this method is somewhat similar to the index() method. The major difference being that index() raises an exception if value is absent whereas find() does not.

12. `index()` - The index() method searches for the first occurrence of the given value and returns the index where it is present. If given value is absent from the string then raise an exception.
```python
                print("hello".index("e"))
```
As we can see, this method is somewhat similar to the find() method. The major difference being that index() raises an exception if value is absent whereas find() does not.

13. `isalnum()` - The isalnum() method returns True only if the entire string only consists of A-Z, a-z, 0-9. If any other characters or punctuations are present, then it returns False
```python
print("hello1".isalnum())
```
14. `isalpha()` - The isalnum() method returns True only if the entire string only consists of A-Z, a-z. If any other characters or punctuations or numbers(0-9) are present, then it returns False.
```python
print("hello".isalpha())
```
15. `islower()` - The islower() method returns True if all the characters in the string are lower case, else it returns False.
```python
 print("Hello".islower())  # returns false
```
16. `isprintable()` - The isprintable() method returns True if all the values within the given string are printable, if not(like \n is not printable), then return False.
```python
print("hello".isprintable())
```
17. `isspace()` - The isspace() method returns True only and only if the string contains white spaces, else returns False. It considers both spacebars and whitespaces
```python
print("  hello".isspace())
```
18. `istitle()` - The istitle() returns True only if the first letter of each word of the string is capitalized, else it returns False.
```python
print("Hello World".istitle())
```
19. `isupper()` - The isupper() method returns True if all the characters in the string are upper case, else it returns False.
```python
print("HELLO".isupper())
```
20. `startswith()` - The endswith() method checks if the string starts with a given value. If yes then return True, else return False.
```python
print("hello".startswith("h"))
```
21. `swapcase()` - The swapcase() method changes the character casing of the string. Upper case are converted to lower case and lower case to upper case.
```python
print("HEllo".swapcase())
```

## If-Else conditional statements in python
Sometimes a programmer needs to take further descisions based on the evaluation of certain expressions as true or false.

This is where conditional statements comes to rescue.

###  Conditional statements are classified as follows:
1. `if`
```python
if(a>5):
        print(a)
```
2. `if-else`
```python
if(a>5):
        print(a)
else:
        print(5)
```

3. `if-else-elif` - Sometimes, the programmer may want to evaluate more than one condition, this can be done using an elif statement.
```python
if(a>5):
        print(a)
elif(a>3):
        print(a+1)
else:
        print(5)
```

4. `nested if-else-elif` - We can use if, if-else, elif statements inside other if statements as well.
```python
if(a>5):
        if(a==7):
        print("true")
        else:
        print("false")
else:
        print("exit")
```

## Match Case statements
Match case is new addition to python(3.10), this is same as switch case statements in c or c++. In c or c++ we need to explicitly use break statement in every case but we dont need to do that in python. A match statement will compare a given variable’s value to different shapes, also referred to as the pattern. The main idea is to keep on comparing the variable with all the present patterns until it fits into one. We can also use if conditions with default case `_` .
```python
    a=4
    match a:
        case 0:
            print("zero")
        case 1:
            print("one")
        case 4:
            print("four")
        case _:
            print("default")     #case _ is default case which executes when no case matches
```

## Loops in Python
Loops are required when sometimes a programmer wants to execute a piece of code certain number of times. Python has following types of loops:

1. for loop
2. while loop
3. nested loops


   1. `For loop` - for loops can iterate over a sequence of iterable objects in python. Iterating over a sequence is nothing but iterating over strings, lists, tuples, sets and dictionaries. We can iterate over strings, lists, dictionaries and many more.
```python
    name="chetan"
    for i in name:
        print(i ,end=" ")
```

Example -
```python
colors=["red","green","blue","yellow"]
for color in colors:
    print(color)
    for i in color:
        print(i)
```

`range()` - this is used when we dont want to iterate over a sequence using for loop instead we want to loop a specific number of times. range() takes parameters as range(start,stop,step)
```python
    for i in range(1,10,2):  #will loop only upto 9 10 is not included
    print(i)
```

   2. `While Loop` - It runs the loop only till a condition is true and terminates it when the condition becomes flase. In Python
`++` increment operator is not supported. Therefore we have to use `variable+=1` instead of `variable++`. Python doesnt have a do while loop.
```python
    i=0
    while(i<3):
        print(i)
        i+=1
```

`Else with while loop` - We can even use the else statement with the while loop. Essentially what the else statement does is that as soon as the while loop condition becomes False, the interpreter comes out of the while loop and the else statement is executed.
```python
    i=0
    while(i<3):
        print(i)
        i+=1
    else:
        print("i is no longer less than 3")
```

The most common technique to emulate a do-while loop in Python is to use an infinite while loop with a break statement wrapped in an if statement that checks a given condition and breaks the iteration if that condition becomes true:
```python
    a=int(input("Enter a number: "))
    while True:
        print("hello")
        if(a==5):
            break
```

## Break and continue statement
1. `break` - The break statement enables a program to skip over a part of the code. A break statement terminates the very loop it lies within.
```python
for i in range(1,11):
    print(i)
    if(i==5):
        break
```

2. `continue` - The continue statement skips the rest of the loop statements and causes the next iteration to occur.
```python
   for i in range(1,11):
    if(i==5):
        continue
    else:
        print(i)
```

## Functions In Python
When we have written a piece of code or program and want to use it over and over at different places in the program we develop a function so that we dont have to write the same code again and again and in case of any changes we will change the code only at one place.

There are two types of functions:

1. `Built-in functions` - These functions are defined and pre-coded in python. Some examples of built-in functions are as follows:
`min()`, `max()`, `len()`, `sum()`, `type()`, `range()`, `dict()`, `list()`, `tuple()`, `set()`, `print()` etc.

2. `User-defined functions` - We can create functions to perform specific tasks as per our needs. Such functions are called user defined functions.

    syntax:
```python
        def funcname(parameters):
            #code of statements
```
    
Example:
```python
        def add(a,b):
            return a+b
        print(add(4,5))
```

If sometimes a developer wants to write the function defination later he can use the pass keyword.
```python
    def funcname(arguments):
        pass
```

Example-
```python
        def add(a,b):
            pass
        print("Defination will be written later")
        def add(a,b):
            return a+b
        print(add(4,5))
```

## Function arguments
There are four types of arguments that we can provide in a function:

1. Default Arguments
2. Keyword Arguments
3. Variable length Arguments
4. Required Arguments

   1. `Default Arguments` - We can provide a default value while creating a function. This way the function assumes a default value even if a value is not provided in the function call for that argument.
```python
    def avg(a=9,b=7):
        print("avg is: ",(a+b)/2)
    avg()
    avg(7)
    avg(5,9)
```

   2. `Keyword Arguments` - We can provide arguments with key = value, this way the interpreter recognizes the arguments by the parameter name. Hence, the the order in which the arguments are passed does not matter.
```python
    def avg(a=9,b=7):
        print("avg is: ",(a+b)/2)
    avg(b=7,a=1) #here we can change the order of arguments
```

   3. `Required Arguments` - When we dont pass deafult value in functiion prototype and even doesnt pass key value as argument while calling function it is necessary to pass number of values as arguments matching the function defination these arguments are called required arguments because they are necessary for execution of the function.
```python
    def avg(a,b=7):
        print("avg is: ",(a+b)/2)
    avg() #here a is a required argument and b is a default argument
```

   4. `Variable length argument` - Sometimes we may need to pass more arguments than those defined in the actual function. This can be done using variable-length arguments.

There are two ways to achieve this:

1. `Arbitrary Arguments`:
While creating a function, pass a * before the parameter name while defining the function. The function accesses the arguments by processing them in the form of tuple.
```python
            def avg(*numbers):
                sum=0
                for number in numbers:
                    sum=sum+number
                print("avg is :",sum/len(numbers))
            avg(1,2,3,4,5,6,7,8,9,10) #arguemnts are passed as tuple because of * in function defination
```

2. `Keyword Arbitrary Arguments`:
While creating a function, pass  ** before the parameter name while defining the function. The function accesses the arguments by processing them in the form of dictionary.
```python
            def printname(**names):
                print("hello",names["fname"],"your age is ",names["age"])
            printname(fname="chetan",age=20) #arguemnts are passed as dictionary because of ** in function defination
```

`Return statement` - The return statement is used to return the value of the expression back to the calling function. If there are more than 1 return statement in a function it will only execute the first and exit the function.
```python
    def add(a,b):
        return a+b
    c=add(4,7)
    print(c)
```

## Lists in Python

1. Lists are ordered collection of data items.
2. They store multiple items in a single variable.
3. List items are separated by commas and enclosed within square brackets [].
4. Lists are changeable meaning we can alter them after creation(but we cannot change tuples they are immutable).
5. List can hold more than one type of datatype
   
syntax-
`listname=[data1,data2,datan]`

The indexing of list also starts with zero so first element can be accessed by `listname[0]`.There is also negative indexing present where `listname[-3]` is same as  `listname[len(listname)-3]` this is the method to convert negative indexing to positive indexing.

To check whether an item is present in the list we can use the in keyword
```python
    number=[1,2,3,4,5,6,7,8,9,10]
    if 7 in number:
        print("yes")
```
Same thing can be done in string also:
```python
    if "che" in "chetan":
        print("yes")
```

### Range of index in lists
You can print a range of list items by specifying where you want to start, where do you want to end and if you want to skip elements in between the range.

syntax-

`listName[start : end : jumpIndex]`
Example-
```python
        number=[1,2,3,4,5,6,7,8,9,10]
        print(number[:]) #prints all elements
        print(number[::2]) #prints all elements with step size 2
        print(number[::-1]) #prints all elements in reverse order
        print(number[2:5:3]) #prints elements from index 2 to 4 with step of 3
```

### List Comprehension
List comprehensions are used for creating new lists from other iterables like lists, tuples, dictionaries, sets, and even in arrays and strings.It is like creating a list on the go

Syntax-

    `List = [Expression(item) for item in iterable if Condition]`

1. `Expression`: It is the item which is being iterated.
2. `Iterable`: It can be list, tuples, dictionaries, sets, and even in arrays and strings.
3. `Condition`: Condition checks if the item should be added to the new list or not.

Example-
```python
    names=["chetan","rahul","rohan","shubham","gokul","rohit"]
    list2=[name for name in names if "h" in name]
    print(list2)
```

### List Methods
1. `sort()` - This method sorts the list in ascending order. The original list is updated
        `list.sort() #sorts in ascending`
   
        `list.sort(reverse=True) #sorts in descending`

2. `reverse()` - This method reverses the order of the list.
        `list.reverse()`

3. `index()` - This method returns the index of the first occurrence of the list item.
        `list.index(item)`

4. `count()` - Returns the count of the number of items with the given value.
        `list.count(item)`

5. `copy()` - Returns copy of the list. This can be done to perform operations on the list without modifying the original list.
        `newlist=oldlist.copy()`

6. `append()` - This method appends items to the end of the existing list.
        `list.append(item to append)`

7. `insert()` - This method inserts an item at the given index. User has to specify index and the item to be inserted within the `insert()` method.
        `list.insert(index,item)`

8. `extend()` - This method adds an entire list or any other collection datatype (set, tuple, dictionary) to the existing list.
        `list0.extend(list1) #items of list 1 gets added to list 0`

We can also concatinate two list and store it in third like this :

`list3=list1+list2`

## Python Tuples
Tuples are same as lists the only difference is that you cannot change a tuple. If you create a tuple with only one element is is necessary to put a `,` after that or else python will interpret it as the datatype of the 
element and not tuple.

syntax
```python
    tuplename=(elemen1,element2,elementn)
    tuplename=(7,) # creating tuple with one element we cant create like (7) as it will show tuplename type then as int
```

Tuples are used by programmers when they want a constant list in a complex program

`Slicing`, `accessing elements through index` and `finding element using "in" keyword` is same in tuple as lists

### Methods of tuple
Tuples are immutable if you want to make any changes in the tuple then first the copy of the tuple has to be converted into list and then the operations can be performed.
```python
    newtup=(1,2,3,4,5,6,7,8,9,10)
    print(newtup)
    temp=list(newtup) #converting tuple to a temporary list
    temp.append(11)
    temp[0]=7
    newtup=tuple(temp) #converting list back to tuple
    print(newtup)
```

We can directly concatinate two tuples because then we are creating a third tuple and not modifying the old tuples
    `tuple3=tuple1+tuple2`

### Tuple supports
1. `count()` - The count() method of Tuple returns the number of times the given element appears in the tuple.
        `tuple.count(element)`
2. `index()` -  The Index() method returns the first occurrence of the given element from the tuple.
    `tuple.index(element)`
We can also find index of an item while slicing
   
syntax-
        `tuple.index(element,start,end)`
example-
```python
        newtup=(1,2,3,4,5,67,3,8,9,10)
        print(newtup.index(3,4,10))
```

### fstrings in python
It is also known as Literal String Interpolation or more commonly as F-strings (f character preceding the string literal). The primary focus of this mechanism is to make the interpolation easier.

We can do this type of string formatting in python
```python
    a="hello my name is {}"
    print(a.format("chetan"))
```

This is not so convinient so we use fstring so that variables can be directly places into string
```python
    money=637392.4483883
    name="chetan"
    country="India"
    a=f"hello my name is {name} and my country is {country} and money is{money:.2f}" #.2f tells to take only 2 decimal places
    print(a)
```
If you want to display word as it is without replacing it with value you can use fstring like this:
```python
f"hello my name is {{name}} and my country is {{country}} # it will not replace value and print direcly {name} and {country}
```
We can use fstring in single statement as well
```python
    print(f"{7*7}") #will print 49
```

### Docstrings in python
Docstrings are just like comments which are given right after function prototype and before writing the actual defination. It tells a lot about the function like its operation no of input its excepts and much more they are generally ignored like comments but if a programmer want to display the docstring it can be diaplyed like this:
```python
    print(funcname.__doc__)
```

As mentioned above, Python docstrings are strings used right after the definition of a function, method, class, or module. They are used to document our code. We can access these docstrings using the doc attribute.

Example-
```python
    def square(n):
        '''Takes in a number n, returns the square of n''' #will be considered as a docstring and not a multiline comment
            return n**2
    print(square.__doc__)
```

### pep8(python enhancement proposal)
PEP 8 is a document that provides guidelines and best practices on how to write Python code. It was written in 2001 by Guido van Rossum, Barry Warsaw, and Nick Coghlan. The primary focus of PEP 8 is to improve the readability and consistency of Python code.

zen of python is a poem which is an easter egg which can be seen when we write import this , it is a simple poem which tells a lot about how to write a python program

### Recursion in Python
In Python, we know that a function can call other functions. It is even possible for the function to call itself. These types of construct are termed as recursive functions.
```python
    def factorial(n):
        if(n==0 or n==1):
            return 1
        else:
            return n * factorial(n-1)
    print(factorial(5))
```

### Sets in Python
As studied in methamatics set is a collection of well defined objects or unordered collection of data items.Set items are separated by commas and enclosed within curly brackets {}. Sets are unchangeable, meaning you cannot change items of the set once created. Sets do not contain duplicate items.

syntax:
```python
    a={2,4,2,6}
    print(a)
```

we cannot create an empty set by using {} because it will be considered as a dictionary to create an empty set Always use `set()`.

### Sets methods in Python
1. `union()` and `update()` - The `union()` and `update()` methods prints all items that are present in the two sets. The `union()` method returns a new set whereas `update()` method adds item into the existing set from another set.
   
Example-
```python
            a={1,4,45,4,6}
            b={1,6,7,4,8,9}
            c=a.union(b)  #union of a and b
            print(c)
            a.update(b)   #updates a with b
            print(a)
```
    
2. `intersection()` and `intersection_update()` - The `intersection()` and `intersection_update()` methods prints only items that are similar to both the sets. The `intersection()` method returns a new set whereas `intersection_update()` method updates into the existing set from another set.
   
Example-
```python
            a={1,4,45,4,6}
            b={1,6,7,4,8,9}
            c=a.intersection(b)  #intersection of a and b
            print(c)
            a.intersection_update(b)   #updates a with intersection of a and b
            print(a)
```
    
3. `symmetric_difference()` and `symmetric_difference_update()` - symmetric difference refers to the values  which are not common to both the sets or the values which are unique to both of the sets. The symmetric_difference() method returns a new set whereas symmetric_difference_update() method updates into the existing set from another set.

Example-
```python
            a={1,4,45,4,6}
            b={1,6,7,4,8,9}
            c=a.symmetric_difference(b)  #symmetric difference of a and b
            print(c)
            a.symmetric_difference_update(b)   #updates a with symmetric difference of a and b
            print(a)
```

4. difference() and difference_update() - difference method returns items which are only present in the original set and not common to the both sets.
    The difference() method returns a new set whereas difference_update() method updates into the existing set from another set.
    example-
            a={1,4,45,4,6}
            b={1,6,7,4,8,9}
            c=a.difference(b)  #difference of a and b
            print(c)
            a.difference_update(b)   #updates a with difference of a and b
            print(a)

    5. isdisjoint() - returns true if there are no common values between two sets otherwise false
            set1.disjoint(set2)
    
    6. issuperset() - checks if the original set contains all values of other set.
    example-
            a={1,4,4,4,6}
            b={1,6,7,4,8,9}
            print(b.issuperset(a)) #checks if b is superset of a
            #returns true becuase b contains all elements of a 
    
    7. issubset() - checks if all item of the given set are present in the original set.
    example-
            a={1,4,4,4,6}
            b={1,6,7,4,8,9}
            print(a.issubset(b)) #checks if a is subset of b
            #returns true becuase all elements of a are present in b
    
    8. add() - to add single item to set
        set1.add(item)
    
    9. remove()/discard() - use to remove item from list. The main difference between remove and discard is that, if we try to delete an item which is not present in set, then remove() raises an error, whereas discard() does not raise any error.
        set1.remove(item)
    
    10. pop() - pop generally removes last item in  python but as set are unordered we will never know which item is going to be removed.
        set.pop()
    
    11. del - del is not a method rather a keyword which deletes the entire set 
        del setname
    
    12. clear() - clears all items in the set and prints an empty set.
        set1.clear()

check like this if an item exits in a set :
        a={1,4,4,4,6}
        b={1,6,7,4,8,9}
        if 1 in a:
            print("yes")
        else:
            print("no")

#Dictionaries in Python
Dictionaries are ordered collection of data items arranged in key:value pairs
example-
    dict1={"name":"chetan","age":20,"city":"mumbai"}
    print(dict1)
    print(dict1["name"]) #will throw error if key is not present
    print(dict1.get("name")) #will print none if key is not present

Accessing keys in Dictionaries
example-
    dict1={"name":"chetan","age":20,"city":"mumbai"}
    print(dict1.keys())
    #or
    for key in dict1.keys():
        print(key)
similarly values can be accessed by 
    print(dict1.values()) #prints all values
    print(dict1[key]) #prints single value corresponding to key

printing key value pairs
    dict1={"name":"chetan","age":20,"city":"mumbai"}
    print(dict1.items()) # items() is used to print key value pairs

## Dictionary methods
    1. update() - used to update one dictionary with a new value or with a new dictionary.
        dict1.update({"age":20}) #update age key if available if not creates a new key value
    2. clear() - clears all items from the dictionary and prints an empty Dictionary
        dict1.clear()
    3. pop() - removes key value pair who's key is passed as parameter
        dict1.pop("key")
    4. popitem() - removes the last key:value pair from the dictionary
        dict1.popitem()
    5. del - this is a keyword which can also be used to delete an item from the dictionary but if any key is not provided it will
    delete the whole dictionary
        del dict1["key"] # deletes a single item
        del dict1 # deletes the dictionary

# for loop with else
In python else can not only be used with if but with for and while loop also. The control is given to else block ones the condition gets false in the loop
    for i in range(0,5):
        print(i)
    else:
        print("loop ended")

Exception Handling in python
    Exception handling is the process of responding to unwanted or unexpected events when a computer program runs. Exception handling deals with these events to avoid the program or system crashing, and without this process, exceptions would disrupt the normal operation of a program.
    When these exceptions occur, the Python interpreter stops the current process and passes it to the calling process until it is handled. If not handled, the program will crash.

    try and except:
        it is used in python when we know that the program may give error or in some cases we dont even know if the server would
        give error at some point of time. We define the try block with the code to execute but if due to some reason let it be wrong user input or dead server
        if the try code is unable to execute then the program will not terminate it will execute the except block and then move forward with next lines of code.
            syntax-
            try:
                #statements which could generate 
                #exception
            except:
                #Soloution of generated exception
            
            example-
                b=[4,5]
                try:
                    a=int(input("enter a number"))
                    for i in range(0,5):
                        print((a*i)+b[i])
                except ValueError:
                    print("value error occured")
                except IndexError:
                    print( "index error occured")

#Finally keyword in python
The block of code written inside finally clause is executed always irrespective of the retun of the values from try or except blocks in a function. This fianlly clause may be used for various purposes like closing some resourse files, closing the database connections or ending the program with some appreciative messages. Generally used for clean up tasks

Example-
    def func1(n):
        try:
            list1=[2,3,4,5,6,7,8,9,10]
            print(list1[n])
            return 1
        except IndexError :
            print("index error occured")
            return 0
        except TypeError:
            print("type error occured")
            return 0
        finally:
            print("function ended") # will execute even after function returns a value
    func1("ch")

# Raising Custom errors
    In python we can raise custom errors using raise keyword it is important to handle errors with which python cannot handle itself (builtin) so that
    our code do not produces any abnormal behaviour. Handling error means dealing with error when some user enters wrong input whereas raising errors means 
    raising custom errors when when some event occurs.

# Defining Custom Exceptions
Sometimes we might want to perform something when a custom error occurs in that case we define the custom exceptions.In Python, we can define custom exceptions by creating a new class that is derived from the built-in Exception class.
For example, sending an error report to the admin, calling an api, etc.
syntax-
    class CustomError(Exception):
    # code ...
    pass
    try:
    # code ...
    except CustomError:
    # code...

#Short hand if else
One line if else statement, with 3 conditions:
a=330
b=435
print(a) if a>b else print(b) if a<b else print(a"="b)
However, it's not suitable for more complex situations where you need to execute multiple statements or perform more complex logic. In those cases, it's best to use the full if-else syntax.

#Enumerate function
Enumerate function helps to get the value as well as index of elements in string tuple lists etc while using a for loop simultaniously.
    marks=[23,45,67,89,90]
    for index,mark in enumerate(marks):
        print(mark)
        if(index==3):
            print("index is 3")

By defaut indec in enumerate starts with 0 but we can change the starting index by passing it as an argument to the enumerate function
    marks=[23,45,67,89,90]
    for index,mark in enumerate(marks,start=1):
        print(mark)
        if(index==3):
            print("index is 3")

#Virtual environment in python
Virtual environment can be created in python using venv keyword it basically means creating many isolated environments on a single machine.
The virtual environment has no relation with the home environment of the pc and is like a fresh python on fresh pc it is genrally used to avoid
package conflicts when many developers are working on the same project because it they use their home environemnt there may be a dissimilarity in their
packages and versions.

    # Create a virtual environment
    python -m venv myenv

    # Activate the virtual environment (Linux/macOS)
    source myenv/bin/activate

    # Activate the virtual environment (Windows)
    myenv\Scripts\activate.bat

    # Deactivate the virtual environment
    deactivate

#Requirements.txt 
reuirements.txt is a file that contain all the packages with their versions that you have used in your project. This file
can easily be use to download all those packages in a new environment in a single go.Using a virtual environment and a requirements.txt file can help you manage the dependencies for your Python projects and ensure that your projects are portable and can be easily set up on a new machine.

    # Output the list of installed packages and their versions to a file
    pip freeze > requirements.txt

    To install the packages listed in the requirements.txt file, you can use the pip install command with the -r flag:

    # Install the packages listed in the requirements.txt file
    pip install -r requirements.txt

#import working in python
Importing in Python is the process of loading code from a Python module into the current script. This allows you to use the functions and variables defined in the module in your current script, as well as any additional modules that the imported module may depend on.
    import math 
    math.sqrt(9)

from keyword - use to import specific function or variable from a module
    from math import sqrt,pi #we can import multiple functions using ","
    c=sqrt(9)*pi
    print(c)

we can also import everything from a module using * but it is not recommended as it might lead to confusion
    from math import *

"as" keyword - as keyword is like giving an alias name to the module you are importing to improve code readability
import pandas as pd 
pd.__version__ #we can now use pd directly

"dir" - Python has a built-in function called dir that you can use to view the names of all the functions and variables defined in a module. This can be helpful for exploring and understanding the contents of a new module.
import math
print(dir(math))

we can also import our custom functions and variables from our another python script
    from filename import function_name,variable_name

#
The if __name__ == "__main__" idiom is a common pattern used in Python scripts to determine whether the script is being run directly or being imported as a module into another script.

In Python, the __name__ variable is a built-in variable that is automatically set to the name of the current module. When a Python script is run directly, the __name__ variable is set to the string __main__ When the script is imported as a module into another script, the __name__ variable is set to the name of the module.
if we import a script as module directly it runs automatically if we only want to use some function of it we can either specify function using "from" or in the script being imported
as module we can write 
if __name__="__main__" #this ensures that the other code runs only when the environment of execution is main

#script to import as module

    def welcome():
        print("Welcome to the world of Python with Chetan")
    if __name__ == "__main__":
        welcome()

#main script
    import chetan
    chetan.welcome()

#OS module in python
The os module in Python is a built-in library that provides functions for interacting with the operating system. It allows you to perform a wide variety of tasks, such as reading and writing files, interacting with the file system, and running system commands.
example-
    import os

    if(not os.path.exists("newfolder")):
        os.mkdir("newfolder")
        for i in range(0,5):
            os.mkdir("newfolder/new"+str(i))
            os.rename("newfolder/new"+str(i),"newfolder/newrenamed"+str(i))
    print(os.listdir("newfolder"))

To execute system commands we can use os.system("command")
You can also use the os.popen function to run a command and get the output as a file-like object:
    import os

    # Run the "ls" command and get the output as a file-like object
    f = os.popen("ls")

    # Read the contents of the output
    output = f.read()
    print(output)  # Output: ['myfile.txt', 'otherfile.txt']

    # Close the file-like object
    f.close()

Reading and writing files The os module provides functions for opening, reading, and writing files. For example, to open a file for reading, you can use the open function:
import os

    # Open the file in read-only mode
    f = os.open("myfile.txt", os.O_RDONLY)

    # Read the contents of the file
    contents = os.read(f, 1024)

    # Close the file
    os.close(f)

#Local vs Global variable in python
A local variable is a variable that is defined inside a function and gets destroyed as soon whereas a global variable is accesible from any function in the code
    x=10
    def func1():
        x=5
        y=7
        print(y)
    func1()
    print(x) #This will not print 5 because x is a global variable and it is not changed in the function

we can use global keyword to edit the global variable inside a function like this -
    x=10
    def func1():
        global x
        x=5
        y=7
        print(y)
    func1()
    print(x) #This will not print 5 because x is a global variable and it is not changed in the function

It's important to note that it's generally considered good practice to avoid modifying global variables from within functions, as it can lead to unexpected behavior and make your code harder to debug.

#File I/O in python
Opening a file      
    f=open("filename","mode")
    f=open("file1.txt","r")

    Various modes are -
    1. (read)r - This mode opens the file for reading only and gives an error if the file does not exist. This is the default mode if no mode is passed as a parameter.
    2. (write)w - This mode opens the file for writing only and creates a new file if the file does not exist.
    3. (append)a - This mode opens the file for appending only and creates a new file if the file does not exist.
    4. (create)x - This mode creates a file and gives an error if the file already exists.
    5. (text)t -  Apart from these modes we also need to specify how the file must be handled. t mode is used to handle text files. t refers to the text mode. There is no difference between r and rt or w and wt since text mode is the default. The default mode is 'r' (open for reading text, synonym of 'rt' ).
    6. (binary)b - used to handle binary files (images, pdfs, etc).

Reading from a file
we can read using read() function
    f=open("file1.txt","r")
    text=f.read()
    print(text)
    f.close()

Writing to a file
    f=open("file1.txt","w")
    f.write("hello world")
    f.close()

Closing a file
It is important to close a file after you are done with it. This releases the resources used by the file and allows other programs to access it.

To close a file, you can use the close() method.

with keyword
if we dont wan to close file again and again we can use with statement to automatically close file
    with open("file1.txt","r") as f:
        print(f.read())

Other file methods
    1. readline() - The readline() method reads a single line from the file. If we want to read multiple lines, we can use a loop.
        with open("file1.txt","r") as f:
        while True:
            line=f.readline()
            if(not line):
                break
            print(line)
    
    2. writelines() - The writelines() method in Python writes a sequence of strings to a file. The sequence can be any iterable object, such as a list or a tuple.
        list1=[1,2,3,4,5,6,7,8,9,10]
        with open("file1.txt","w") as f:
                f.writelines(str(list1))
    
    3. seek() - with the help of seek function the current position whithin the file can be moved and data can be read from that specific position
        with open("file1.txt","r") as f:
            f.seek(4) #moves the cursor to 4th position
            data=f.read(5)
            print(data)
    
    4.tell() - tell() function helps to tell us the current position of the cursor within the file. This can be useful for keeping track of your location within the file or for seeking to a specific position relative to the current position.
            with open("file1.txt","r") as f:
                f.seek(4) #moves the cursor to 4th position
                data=f.read(5)
                print(data)
                print(f.tell()) #current position of cursor

     5. truncate() - it is used to remove all characters in a file upto a specific position. it can only be used with write and append modes
        with open("file1.txt","w") as f:
            f.write("hello world")
            f.truncate(3)

#lambda functions
Lambda functions are the functions which are used for writing short functions this functions are are genrally defined in a variable which is used as the function name or they can be used directly without name (anonymously)
Lambda functions are often used in situations where a small function is required for a short period of time. They are commonly used as arguments to higher-order functions, such as map, filter, and reduce
    sum=lambda x:x+=x
    print(sum(5))
example-
    # Lambda function to calculate the product of two numbers,
    # with additional print statement
    lambda x, y: print(f'{x} * {y} = {x * y}')

#Map , Filter and reduce
Map function applies the given function to each element in a sequence and returns a new map object
    list1=[1,2,3,4,5,6,7,8,9,10]
    newlist=list(map(lambda x:x*2,list1))
    print(newlist)
    
Filter function filter elements based on a boolean condition in the functions passed and returns a new sequence containing elements meeting the condition
    list1=[1,2,3,4,5,6,7,8,9,10]
    newseq=filter(lambda x: x>5,list1)
    print(list(newseq))

Higher order functions are those functions which take function as an argument

reduce
we have to import reduce in order to use it first
    from functools import reduce
reduce helps to reduce a an iterable to a single value
    from functools import reduce
    list1=[1,2,3,4,5,6,7,8,9,10]
    newseq=reduce(lambda x,y: (x+y),list1) #this  will work like 1+2=3,3+3=6,6+4=10,10+5=15,15+6=21,21+7=28,28+8=36,36+9=45,45+10=55
    print(newseq)

#is vs ==
is compares exact location of object in memory whereas "==" compares values of objects
when immutable things are created in python like a tuple or constant and same thing is created with another variable name then
python only assigns memory once and other variable is made to point to that location

a=4
b=4 #because both are constant b will point to memory location of a 
print(a is b) # willl print true

#Object Oriented programming in Python
 In programming languages, mainly there are two approaches that are used to write program or code.

1. Procedural Programming
2. Object-Oriented Programming

The procedure we are following till now is the “Procedural Programming” approach. So, in this session, we will learn about Object Oriented Programming (OOP). The basic idea of object-oriented programming (OOP) in Python is to use classes and objects to represent real-world concepts and entities.

A class is a blueprint or template for creating objects. It defines the properties and methods that an object of that class will have. Properties are the data or state of an object, and methods are the actions or behaviors that an object can perform.

An object is an instance of a class, and it contains its own data and methods. For example, you could create a class called "Person" that has properties such as name and age, and methods such as speak() and walk(). Each instance of the Person class would be a unique object with its own name and age, but they would all have the same methods to speak and walk.

One of the key features of OOP in Python is encapsulation, which means that the internal state of an object is hidden and can only be accessed or modified through the object's methods. This helps to protect the object's data and prevent it from being modified in unexpected ways.

Another key feature of OOP in Python is inheritance, which allows new classes to be created that inherit the properties and methods of an existing class. This allows for code reuse and makes it easy to create new classes that have similar functionality to existing classes.

Polymorphism is also supported in Python, which means that objects of different classes can be treated as if they were objects of a common class. This allows for greater flexibility in code and makes it easier to write code that can work with multiple types of objects.

    class person:
        name="chetan"
        age=20
        occupation="student"
        def info(self): #self keyword refers to current instance of the class or object on which the function is called
            print(f"{self.name} is {self.occupation}")

    object1=person()
    object1.occupation="cyber security expert"
    object1.info()

#constructors in python
Constructor is a special method in a class that is used to initialize objects. Constructor is invoked automatically as soon as an object is created
There are 2 types of constructors-
    1. parameterized constructor - which take arguments along with self
    2. Default constructor - which only takes self as argument
        class person:
            name="chetan"
            age=20
            occupation="student"
            def __init__(self,name1,occ): #this is a constructor created by __constructorname__
                self.name=name1
                self.occupation=occ
            def info(self):
                print(f"{self.name} is {self.occupation}")

        object1=person("goku","HR")
        object1.info()

#Decorators in Python
A decorator takes a function as an argument then modifies it and returns a new function which is refrred to as decorated function
synax-
    @decorator_function
    def my_function():
        pass

Note - in a function *args is used to accept arguments as tuple(positional argument) and **args is used to accept arguments as dictionary(keyword arguments)
    def greet(fx):
        def mfx(*args,**kwargs):
            print("Welcome")
            fx(*args,**kwargs)
            print("Bye")
        return mfx

    @greet
    def add(number,number2):
        print(number+number2)

    @greet
    def hello():
        print("hello world")

    add(number=2,number2=3)

In conclusion, python decorators are a way to extend the functionality of functions and methods, by modifying its behavior without modifying the source code. They are used for a variety of purposes, such as logging, memoization, access control, and more. They are a powerful tool that can be used to make your code more readable, maintainable, and extendable.



