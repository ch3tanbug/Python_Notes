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

4. `difference()` and `difference_update()` - difference method returns items which are only present in the original set and not common to the both sets. The difference() method returns a new set whereas difference_update() method updates into the existing set from another set.
   
Example-
```python
            a={1,4,45,4,6}
            b={1,6,7,4,8,9}
            c=a.difference(b)  #difference of a and b
            print(c)
            a.difference_update(b)   #updates a with difference of a and b
            print(a)
```

5. `isdisjoint()` - returns true if there are no common values between two sets otherwise false

`set1.disjoint(set2)`
    
6. `issuperset()` - checks if the original set contains all values of other set.
   
Example-
```python
            a={1,4,4,4,6}
            b={1,6,7,4,8,9}
            print(b.issuperset(a)) #checks if b is superset of a
            #returns true becuase b contains all elements of a
```
    
7. `issubset()` - checks if all item of the given set are present in the original set.
   
Example-
```python
            a={1,4,4,4,6}
            b={1,6,7,4,8,9}
            print(a.issubset(b)) #checks if a is subset of b
            #returns true becuase all elements of a are present in b
```
    
8. `add()` - to add single item to set
   
`set1.add(item)`
    
9. `remove()/discard()` - use to remove item from list. The main difference between remove and discard is that, if we try to delete an item which is not present in set, then remove() raises an error, whereas discard() does not raise any error.
    
`set1.remove(item)`
    
10. `pop()` - pop generally removes last item in  python but as set are unordered we will never know which item is going to be removed.

`set.pop()`
    
11. `del` - del is not a method rather a keyword which deletes the entire set
    
`del setname`
    
12. `clear()` - clears all items in the set and prints an empty set.
    
`set1.clear()`

Check like this if an item exits in a set :
```python
        a={1,4,4,4,6}
        b={1,6,7,4,8,9}
        if 1 in a:
            print("yes")
        else:
            print("no")
```

## Dictionaries in Python
Dictionaries are ordered collection of data items arranged in `key:value` pairs.

Example-
```python
    dict1={"name":"chetan","age":20,"city":"mumbai"}
    print(dict1)
    print(dict1["name"]) #will throw error if key is not present
    print(dict1.get("name")) #will print none if key is not present
```

### Accessing keys in Dictionaries
Example-
```python
    dict1={"name":"chetan","age":20,"city":"mumbai"}
    print(dict1.keys())
    #or
    for key in dict1.keys():
        print(key)
```
Similarly values can be accessed by :
```python
    print(dict1.values()) #prints all values
    print(dict1[key]) #prints single value corresponding to key
```

Printing key value pairs:
```python
    dict1={"name":"chetan","age":20,"city":"mumbai"}
    print(dict1.items()) # items() is used to print key value pairs
```

### Dictionary methods

1. `update()` - used to update one dictionary with a new value or with a new dictionary.
```python
        dict1.update({"age":20}) #update age key if available if not creates a new key value
```
2. `clear()` - clears all items from the dictionary and prints an empty Dictionary
```python
        dict1.clear()
```
3. `pop()` - removes key value pair who's key is passed as parameter
```python
        dict1.pop("key")
```
4. `popitem()` - removes the last key:value pair from the dictionary
```python
        dict1.popitem()
```
5. `del` - this is a keyword which can also be used to delete an item from the dictionary but if any key is not provided it will delete the whole dictionary.
```python
        del dict1["key"] # deletes a single item
        del dict1 # deletes the dictionary
```

## for loop with else
In python else can not only be used with if but with for and while loop also. The control is given to else block ones the condition gets false in the loop.
```python
    for i in range(0,5):
        print(i)
    else:
        print("loop ended")
```

## Exception Handling in python
Exception handling is the process of responding to unwanted or unexpected events when a computer program runs. Exception handling deals with these events to avoid the program or system crashing, and without this process, exceptions would disrupt the normal operation of a program. When these exceptions occur, the Python interpreter stops the current process and passes it to the calling process until it is handled. If not handled, the program will crash.

### try and except:
It is used in python when we know that the program may give error or in some cases we dont even know if the server would give error at some point of time. We define the try block with the code to execute but if due to some reason let it be wrong user input or dead server. If the try code is unable to execute then the program will not terminate it will execute the except block and then move forward with next lines of code.

Syntax-
```python
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
```

## Finally keyword in python
The block of code written inside finally clause is executed always irrespective of the retun of the values from try or except blocks in a function. This fianlly clause may be used for various purposes like closing some resourse files, closing the database connections or ending the program with some appreciative messages. Generally used for clean up tasks

Example-
```python
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
```

## Raising Custom errors
In python we can raise custom errors using raise keyword it is important to handle errors with which python cannot handle itself (builtin) so that our code do not produces any abnormal behaviour. Handling error means dealing with error when some user enters wrong input whereas raising errors means raising custom errors when when some event occurs.

## Defining Custom Exceptions
Sometimes we might want to perform something when a custom error occurs in that case we define the custom exceptions.In Python, we can define custom exceptions by creating a new class that is derived from the built-in Exception class. For example, sending an error report to the admin, calling an api, etc.

Syntax-
```python
    class CustomError(Exception):
    # code ...
    pass
    try:
    # code ...
    except CustomError:
    # code...
```

## Short hand if else
One line if else statement, with 3 conditions:
```python
a=330
b=435
print(a) if a>b else print(b) if a<b else print(a"="b)
```
However, it's not suitable for more complex situations where you need to execute multiple statements or perform more complex logic. In those cases, it's best to use the full if-else syntax.

## Enumerate function
Enumerate function helps to get the value as well as index of elements in string tuple lists etc while using a for loop simultaniously.
```python
    marks=[23,45,67,89,90]
    for index,mark in enumerate(marks):
        print(mark)
        if(index==3):
            print("index is 3")
```

By defaut index in enumerate starts with 0 but we can change the starting index by passing it as an argument to the enumerate function
```python
    marks=[23,45,67,89,90]
    for index,mark in enumerate(marks,start=1):
        print(mark)
        if(index==3):
            print("index is 3")
```

## Virtual environment in python
Virtual environment can be created in python using venv keyword it basically means creating many isolated environments on a single machine. The virtual environment has no relation with the home environment of the pc and is like a fresh python on fresh pc it is genrally used to avoid package conflicts when many developers are working on the same project because it they use their home environemnt there may be a dissimilarity in their packages and versions.

1. Create a virtual environment
`python -m venv myenv`

2. Activate the virtual environment (Linux/macOS)
`source myenv/bin/activate`

3. Activate the virtual environment (Windows)
`myenv\Scripts\activate.bat`

4. Deactivate the virtual environment
`deactivate`

## Requirements.txt 
reuirements.txt is a file that contain all the packages with their versions that you have used in your project. This file
can easily be use to download all those packages in a new environment in a single go.Using a virtual environment and a requirements.txt file can help you manage the dependencies for your Python projects and ensure that your projects are portable and can be easily set up on a new machine.

1. Output the list of installed packages and their versions to a file
`pip freeze > requirements.txt`

To install the packages listed in the requirements.txt file, you can use the pip install command with the -r flag:

2. Install the packages listed in the requirements.txt file
`pip install -r requirements.txt`

## import working in python
Importing in Python is the process of loading code from a Python module into the current script. This allows you to use the functions and variables defined in the module in your current script, as well as any additional modules that the imported module may depend on.
```python
    import math 
    math.sqrt(9)
```

`from keyword` - use to import specific function or variable from a module from math import sqrt,pi #we can import multiple functions using `,`
```python
    c=sqrt(9)*pi
    print(c)
```

We can also import everything from a module using * but it is not recommended as it might lead to confusion
```python
    from math import *
```

1. `as` keyword - as keyword is like giving an alias name to the module you are importing to improve code readability
```python
import pandas as pd 
pd.__version__ #we can now use pd directly
```

2. `dir` - Python has a built-in function called dir that you can use to view the names of all the functions and variables defined in a module. This can be helpful for exploring and understanding the contents of a new module.
```python
import math
print(dir(math))
```

We can also import our custom functions and variables from our another python script
```python
from filename import function_name,variable_name
```

The `if __name__ == "__main__"` idiom is a common pattern used in Python scripts to determine whether the script is being run directly or being imported as a module into another script.

In Python, the `__name__` variable is a built-in variable that is automatically set to the name of the current module. When a Python script is run directly, the `__name__` variable is set to the string `__main__` When the script is imported as a module into another script, the `__name__` variable is set to the name of the module. If we import a script as module directly it runs automatically if we only want to use some function of it we can either specify function using `from` or in the script being imported as module we can write 
```python
if __name__="__main__" #this ensures that the other code runs only when the environment of execution is main
```

Script to import as module:
```python
    def welcome():
        print("Welcome to the world of Python with Chetan")
    if __name__ == "__main__":
        welcome()

#main script
    import chetan
    chetan.welcome()
```

## OS module in python
The os module in Python is a built-in library that provides functions for interacting with the operating system. It allows you to perform a wide variety of tasks, such as reading and writing files, interacting with the file system, and running system commands.

Example-
```python
    import os

    if(not os.path.exists("newfolder")):
        os.mkdir("newfolder")
        for i in range(0,5):
            os.mkdir("newfolder/new"+str(i))
            os.rename("newfolder/new"+str(i),"newfolder/newrenamed"+str(i))
    print(os.listdir("newfolder"))
````

To execute system commands we can use `os.system("command")`

You can also use the `os.popen` function to run a command and get the output as a file-like object:
```python
    import os

    # Run the "ls" command and get the output as a file-like object
    f = os.popen("ls")

    # Read the contents of the output
    output = f.read()
    print(output)  # Output: ['myfile.txt', 'otherfile.txt']

    # Close the file-like object
    f.close()
```

Reading and writing files The os module provides functions for opening, reading, and writing files. For example, to open a file for reading, you can use the open function:
```python
    import os

    # Open the file in read-only mode
    f = os.open("myfile.txt", os.O_RDONLY)

    # Read the contents of the file
    contents = os.read(f, 1024)

    # Close the file
    os.close(f)
````

## Local vs Global variable in python
A local variable is a variable that is defined inside a function and gets destroyed as soon whereas a global variable is accesible from any function in the code
```python
    x=10
    def func1():
        x=5
        y=7
        print(y)
    func1()
    print(x) #This will not print 5 because x is a global variable and it is not changed in the function
```

we can use global keyword to edit the global variable inside a function like this -
```python
    x=10
    def func1():
        global x
        x=5
        y=7
        print(y)
    func1()
    print(x) #This will not print 5 because x is a global variable and it is not changed in the function
```

It's important to note that it's generally considered good practice to avoid modifying global variables from within functions, as it can lead to unexpected behavior and make your code harder to debug.

## File I/O in python
Opening a file 
```python
    f=open("filename","mode")
    f=open("file1.txt","r")
```

Various modes are -
1. (read)`r` - This mode opens the file for reading only and gives an error if the file does not exist. This is the default mode if no mode is passed as a parameter.
2. (write)`w` - This mode opens the file for writing only and creates a new file if the file does not exist.
3. (append)`a` - This mode opens the file for appending only and creates a new file if the file does not exist.
4. (create)`x` - This mode creates a file and gives an error if the file already exists.
5. (text)`t` -  Apart from these modes we also need to specify how the file must be handled. t mode is used to handle text files. t refers to the text mode. There is no difference between r and rt or w and wt since text mode is the default. The default mode is 'r' (open for reading text, synonym of 'rt' ).
6. (binary)`b` - used to handle binary files (images, pdfs, etc).

### Reading from a file

we can read using read() function
```python
    f=open("file1.txt","r")
    text=f.read()
    print(text)
    f.close()
```

### Writing to a file
```python
    f=open("file1.txt","w")
    f.write("hello world")
    f.close()
```

### Closing a file
It is important to close a file after you are done with it. This releases the resources used by the file and allows other programs to access it. To close a file, you can use the `close()` method.

`with` keyword
if we dont wan to close file again and again we can use with statement to automatically close file
```python
    with open("file1.txt","r") as f:
        print(f.read())
```

### Other file methods
1. `readline()` - The readline() method reads a single line from the file. If we want to read multiple lines, we can use a loop.
```python
        with open("file1.txt","r") as f:
        while True:
            line=f.readline()
            if(not line):
                break
            print(line)
```
    
2. `writelines()` - The writelines() method in Python writes a sequence of strings to a file. The sequence can be any iterable object, such as a list or a tuple.
```python
        list1=[1,2,3,4,5,6,7,8,9,10]
        with open("file1.txt","w") as f:
                f.writelines(str(list1))
```
    
3. `seek()` - with the help of seek function the current position whithin the file can be moved and data can be read from that specific position
```python
        with open("file1.txt","r") as f:
            f.seek(4) #moves the cursor to 4th position
            data=f.read(5)
            print(data)
```
    
4.`tell()` - tell() function helps to tell us the current position of the cursor within the file. This can be useful for keeping track of your location within the file or for seeking to a specific position relative to the current position.
```python
            with open("file1.txt","r") as f:
                f.seek(4) #moves the cursor to 4th position
                data=f.read(5)
                print(data)
                print(f.tell()) #current position of cursor
```

5. `truncate()` - it is used to remove all characters in a file upto a specific position. it can only be used with write and append modes
```python
        with open("file1.txt","w") as f:
            f.write("hello world")
            f.truncate(3)
```

## lambda functions
Lambda functions are the functions which are used for writing short functions this functions are are genrally defined in a variable which is used as the function name or they can be used directly without name (anonymously). Lambda functions are often used in situations where a small function is required for a short period of time. They are commonly used as arguments to higher-order functions, such as `map`, `filter`, and `reduce`.
```python
    sum=lambda x:x+=x
    print(sum(5))
example-
    # Lambda function to calculate the product of two numbers,
    # with additional print statement
    lambda x, y: print(f'{x} * {y} = {x * y}')
```

## Map , Filter and reduce
1. `Map` function applies the given function to each element in a sequence and returns a new map object
```python
    list1=[1,2,3,4,5,6,7,8,9,10]
    newlist=list(map(lambda x:x*2,list1))
    print(newlist)
```
    
2. `Filter` function filter elements based on a boolean condition in the functions passed and returns a new sequence containing elements meeting the condition
```python
    list1=[1,2,3,4,5,6,7,8,9,10]
    newseq=filter(lambda x: x>5,list1)
    print(list(newseq))
```

Higher order functions are those functions which take function as an argument

`reduce`

we have to import reduce in order to use it first
```python
    from functools import reduce
```
reduce helps to reduce a an iterable to a single value
```python
    from functools import reduce
    list1=[1,2,3,4,5,6,7,8,9,10]
    newseq=reduce(lambda x,y: (x+y),list1) #this  will work like 1+2=3,3+3=6,6+4=10,10+5=15,15+6=21,21+7=28,28+8=36,36+9=45,45+10=55
    print(newseq)
```

## is vs ==
`is` compares exact location of object in memory whereas `==` compares values of objects when immutable things are created in python like a tuple or constant and same thing is created with another variable name then python only assigns memory once and other variable is made to point to that location
```python
a=4
b=4 #because both are constant b will point to memory location of a 
print(a is b) # willl print true
```

## Object Oriented programming in Python
In programming languages, mainly there are two approaches that are used to write program or code.

1. Procedural Programming
2. Object-Oriented Programming

The procedure we are following till now is the `Procedural Programming` approach. So, in this session, we will learn about Object Oriented Programming (OOP). The basic idea of object-oriented programming (OOP) in Python is to use classes and objects to represent real-world concepts and entities.

A class is a blueprint or template for creating objects. It defines the properties and methods that an object of that class will have. Properties are the data or state of an object, and methods are the actions or behaviors that an object can perform.

An object is an instance of a class, and it contains its own data and methods. For example, you could create a class called "Person" that has properties such as name and age, and methods such as `speak()` and `walk()`. Each instance of the Person class would be a unique object with its own name and age, but they would all have the same methods to speak and walk.

One of the key features of `OOP` in Python is encapsulation, which means that the internal state of an object is hidden and can only be accessed or modified through the object's methods. This helps to protect the object's data and prevent it from being modified in unexpected ways.

Another key feature of OOP in Python is inheritance, which allows new classes to be created that inherit the properties and methods of an existing class. This allows for code reuse and makes it easy to create new classes that have similar functionality to existing classes.

`Polymorphism` is also supported in Python, which means that objects of different classes can be treated as if they were objects of a common class. This allows for greater flexibility in code and makes it easier to write code that can work with multiple types of objects.
```python

    class person:
        name="chetan"
        age=20
        occupation="student"
        def info(self): #self keyword refers to current instance of the class or object on which the function is called
            print(f"{self.name} is {self.occupation}")

    object1=person()
    object1.occupation="cyber security expert"
    object1.info()
```

##  constructors in python
Constructor is a special method in a class that is used to initialize objects. Constructor is invoked automatically as soon as an object is created

There are 2 types of constructors-

1. `parameterized constructor` - which take arguments along with self
2. `Default constructor` - which only takes self as argument
```python
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
```

## Decorators in Python
A decorator takes a function as an argument then modifies it and returns a new function which is refrred to as decorated function

Synax-
```python
    @decorator_function
    def my_function():
        pass
```

Note - in a function `*args` is used to accept arguments as tuple(positional argument) and **args is used to accept arguments as dictionary(keyword arguments)
```python
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
```

In conclusion, python decorators are a way to extend the functionality of functions and methods, by modifying its behavior without modifying the source code. They are used for a variety of purposes, such as logging, memoization, access control, and more. They are a powerful tool that can be used to make your code more readable, maintainable, and extendable.

#3 Getters and Setters
Getters are used with @property decorator and behave like a method is a property of a class. It is important to note that the getters do not take any parameters and we cannot set the value through getter method.For that we need setter method which can be added by decorating method with `@property_name.setter`
```python
class MyClass:
    def __init__(self, value):
        self._value = value

    @property #@property is a decorator built in python
    def ten_value(self): #this is a getter method
        return self._value*10
    @ten_value.setter #setter method
    def ten_value(self, value):
        self.value=value//10
    
obj1=MyClass(10)
print(obj1.ten_value) #ten value is a method but we can access it as a property
obj1.ten_value=100
print(obj1.value)
```

## Inheritance in python
Inheritance is the process of making a new class from already existing class. The class which is used for deriving a new class is called base class and the the new class is called derived class
Syntax-
```python
    class derived(base):
        code
```

Types of classes -
1. `Single inheritance`
2. `Multiple inheritance`
3. `Multilevel inheritance`
4. `Hierarchical Inheritance`
5. `Hybrid Inheritance`

## Access modifiers in python
Access modifiers helps in limiting the access of class variables and methods outside the class

1. `Public access modifier` - All methods and variables are by default public in python
2. `Private access modifier` - In Python, there is no strict concept of "private" access modifiers like in some other programming languages. However, a convention has been established to indicate that a variable or method should be considered private by prefixing its name with a double underscore `__`. This is known as a "weak internal use indicator" and it is a convention only, not a strict rule we can limit the private access by
```python
            self.__variablename=value
```
When we declare variable inside class like this we cant access it by object.variablename directly  but we can access it by `object._classname__variablename`
Example -
```python
            class myclass:
            def __init__(self,value):
            self.__valued=5
            self._value=value
            object1=myclass(10)
            print(object1._value)
            print(object1.__value) #this will give an error because __value is a private variable and it can only be accessed inside the class
            print(object1._myclass__valued) #this will work because __value is a private variable and it can only be accessed inside the class but we can access it outside the class by using _classname__variablename
```

The `__dir__()` method can be used with object to see all methods and attributed available related to the particular class
```python
    print(object1.__dir__())
```

## Name Mangling
Name mangling in Python is a technique used to protect class-private and superclass-private attributes from being accidentally overwritten by subclasses. Names of class-private and superclass-private attributes are transformed by the addition of a single leading underscore and a double leading underscore respectively.

In python there is no concept of private public and protected they are just naming conventions and only when we do `__` the name mangling occurrs others all things  are just naming conventions which are treated as private public and protected

### Protected Access modifiers
In Python, the convention for indicating that a member is protected is to prefix its name with a single underscore `_`. For example, if a class has a method called `_my_method`, it is indicating that the method should only be accessed by the class itself and its subclasses.

It's important to note that the single underscore is just a naming convention, and does not actually provide any protection or restrict access to the member. The syntax we follow to make any variable protected is to write variable name followed by a single underscore `_` ie. `_varName`.

Example-
```python
        class newclass:
        string=""
        def __init__(self):
            self._value=10
        def _newfunc(self,x): # we used _newfunc because it is a protected method as a convention
            self.string=x
            print(self.string)
        class derived(newclass):
            pass
        obj1=derived()
        obj1._newfunc("hello world")
```

## Static methods in python
Static methods in Python are methods that belong to a class rather than an instance of the class. They are defined using the `@staticmethod` decorator and do not have access to the instance of the class (i.e. self). They are called on the class itself, not on an instance of the class. Static methods are often used to create utility functions that don't need access to instance data. But they always remain inside the class as we want some methods should be shipped along the class
Example-
```python
    class math:
        @staticmethod
        def add(x,y):
            return x+y
        print(math.add(2,3)) # no need to call with an object because it is a static method
```

## Class variables vs Instance variables
Class variables are associated with a particular class and are same for all instances unless an explicit change is made Instance variables are variables that are associated with particular instance(object) and maybe different for different objects
When we call a variable in class it first checks if the object has a defined instance variable if not then it moves on and gives the value of class variable

Example-
```python
    class employee:
        company="google" #this is a class variable
        def __init__(self,name):
            self.name=name #this is an instance variable
    obj1=employee("chetan")
    obj2=employee("goku")
    obj1.company="Apple" #this will only change the value of company for obj1 and not for obj2
    print(obj1.company)
    print(obj2.company)
    employee.company="Microsoft" #this will change the value of company for all the objects
    print(obj1.company) #still this will show apple because it is stored in instance variable
    print(obj2.company)
```

## Class Methods in Python
class is way to define custom datatype. Whenever we pass first argument to a method in class it takes it as the object like `def func1(self,number)` here self refers to object and here any modification which we do will only change the instance variables but sometimes. We want to change the class variables inside a method in thata case we use `@classmethod` decorator before function

Example-
```python
    class employee:
        company="google" #this is a class variable
        @classmethod
        def method1(cls,company): #cls refers to the class
            cls.company=company
```

## Class methods as alternative constructors
There are times when you may want to create an object in a different way, or with different initial values, than what is provided by the default constructor. This is where class methods can be used as alternative constructors. you declare a method which first modifies the data by the user to data which the constrcutor can accept and then it is passed to the constructor

Example-
```python
    class person:
        def __init__(self,name,age):
            self.name=name
            self.age=age
        @classmethod
        def fromstr(cls,string): #using methods as alternative constructors
            return cls(string.split("-")[0],string.split("-")[1])
    obj1=person.fromstr("goku-20")
    print(obj1.name)
    print(obj1.age)
```

## dir , __dict__ and help methods in python

1. `dir()` - The dir() function returns a list of all the attributes and methods (including dunder methods) available for an object. It is a useful tool for discovering what you can do with an object.
   
Example-
```python
    list1=[1,2,3,4,5,6,7,8,9,10]
    print(dir(list1))
    print(list1.__dir__())
```

2.`__dict__` - will return all the self  attributes of an object with their value in dictionary

Example-
```python
    class person:
        def __init__(self,name,age):
            self.name=name
            self.age=age
        @classmethod
        def fromstr(cls,string): #using methods as alternative constructors
            return cls(string.split("-")[0],string.split("-")[1])
    obj1=person.fromstr("goku-20")
    print(obj1.__dict__)
```

3. `help()` - it returns documentation of object along with its methods and attributes

Example -
```python
    class person:
        def __init__(self,name,age):
            self.name=name
            self.age=age
        @classmethod
        def fromstr(cls,string): #using methods as alternative constructors
            return cls(string.split("-")[0],string.split("-")[1])
    obj1=person.fromstr("goku-20")
    print(help(obj1)) #returns the documentation of the class
```

## super keyword
`super` keyword refers to the parent class and is used to call the methods of parent class in the child class
Example -
```python
    class employee:
        def __init__(self,name,empid):
            self.name=name
            self.empid=empid
    class programmer(employee):
        def __init__(self,name,empid,language):
            super().__init__(name,empid) #super() is used to call the constructor of the parent class
            self.language=language
    obj1=programmer("chetan",1,"python")
    print(obj1.__dict__)
```

## magic/dunder methods
`magic methods` are those methods in python which are defined as `__methodname__` and can be used directly with their name
i.e `methodname()`

1. `__init__` - it is called automatically when an object is created
2. `__str__` and __repr__ methods - __str__ is used to print out the object whereas __repr__ is used to get string representation of object
so that object can be recreated
3. `__len__` - it is used to get the length of the object 
4. `__call__` - The call method is used to make an object callable, meaning that you can pass it as a parameter to a function and it will be executed when the function is called. This is an incredibly powerful tool that allows you to create objects that behave like functions.

Example-
```python
    class employee:
        def __init__(self,name,empid):
            self.name=name
            self.empid=empid
    class programmer(employee):
        def __init__(self,name,empid,language):
            super().__init__(name,empid) #super() is used to call the constructor of the parent class
            self.language=language
        def __len__(self):
            return len(self.name)
        def __str__(self):
            return f"{self.name} is a programmer"
        def __repr__(self):
            return f"{self.name} is a programmer"
        def __call__(self):
            print(f"this object has been called")
    obj1=programmer("chetan",1,"python")
    print(len(obj1))
    print(str(obj1))
    print(repr(obj1))
    obj1()
```

## Method overriding in python
It is a feature to change the method od parent class in the child class

Example -
```python
    class area:
        def areashape(self,a,b):
            return a*b
    class circle(area):
        def areashape(self,radius): #method overriding
            return 3.14*super().areashape(radius,radius)
    obj1=circle()
    print(obj1.areashape(2))
```

## Operator Overloading
In python operators can be overloaded using dunder methods like __add__ which means + __sub__ which means - and many more(can be read from the official documentation). It facilitates the addition , subtraction and logical operations on objects

1. `+`	__add__(self, other)
2. `–`	__sub__(self, other)
3. `*`	__mul__(self, other)
4. `/`	__truediv__(self, other)
5. `//`	__floordiv__(self, other)
6. `%`	__mod__(self, other)
7. `**`	__pow__(self, other)
8. `>>`	__rshift__(self, other)
9. `<<`	__lshift__(self, other)
10. `&`	__and__(self, other)
11. `|`	__or__(self, other)
12. `^`	__xor__(self, other)

There are a lot more operators which can be overloaded (refer original documentation)

Example-
```python
    class vector:
        def __init__(self,x,y):
            self.x=x
            self.y=y
        def __add__(self,x):
            return vector(self.x+x.x,self.y+x.y)
    obj1=vector(2,3)
    obj2=vector(4,5)
    print((obj1+obj2).x,(obj1+obj2).y)
```

## Exploring types of inheritance
1. `single inheritance` - It is the simplest form of inheritance wherin only a child class inherits properties and methods from a single parent class
   
Syntax-
```python
    class childclass(parentclass):
        code
example-
    class animal:
        def __init__(self,name):
            self.name=name
        def sound(self):
            print("animal sound")
    class dog(animal):
        def sound(self):
            print("dog sound")
    obj1=dog("tommy")
    obj2=animal("animal")
    obj1.sound()
    obj2.sound()
```

2. `Multiple inheritance` -When a child class has more than one parent class it is said to be multiple inheritance
   
Syntax-
```python
    class childclass(parentclass1,parentclass2):
        code
```

Please remember the order in which the parent classes are passed in the child class will decide which function will execute
in case both the parent classes have the same name function the general route for searching a function by interpreter is `childclass->parent class passed first->parent class passed second`

NOTE- __mro__ dunder method or mro() can be used to know how an object will search while executing a function

example-
    class animal:
        def __init__(self,name):
            self.name=name
        def sound(self):
            print("animal sound")
    class dog(animal):
        def sound(self):
            print("dog sound")
    class pet(dog,animal): #multiple inheritance
        def __init__(self,name):
            super().__init__(name)
    obj1=pet("thomp")
    obj1.sound() #this will print dog sound because it will search for sound method in pet class first and then in dog class and then in animal class
    print(pet.__mro__) #this will print the order in which the classes are searched for a method

3. Multilevel Inheritance
Multilevel Inheritance is a type of inheritance in which a child class acts as a base class for the next child class
syntax-
    class baseclass:
        code
    class derived1(baseclass):
        code
    class derived2(derived1):
        code
example-
        class animal():
        def __init__(self,name):
            self.name=name
        def show_details(self):
            print("animal")
    class dog(animal):
        def show_details(self):
            super().show_details()
            print("dog")
    class pug(dog):
        def show_details(self):
            super().show_details()
            print("pug")
    obj1=pug("thomp")
    print(obj1.name)
    obj1.show_details()

4. Hierarchical Inheritance
It is a type of inheritance where multiple classes are derived from a single base class
syntax-
    class BaseClass:
    pass

    class D1(BaseClass):
    pass

    class D2(BaseClass):
    pass

    class D3(D1):
    pass

5. Hybrid Inheritance 
When two or more types of inheritance are combined in a program it creates Hybrid Inheritance
syntax-
    class BaseClass:
    pass

    class Derived1(BaseClass):
    pass  

    class Derived2(BaseClass):
    pass  

    class Derived3(Derived1, Derived2):
    pass

#Time Module in Python
The time module in Python provides a set of functions to work with time-related operations, such as timekeeping, formatting, and time conversions.
we need to do
    import time

    1. time.time() - The time.time() function returns the current time as a floating-point number, representing the number of seconds since the epoch (the point in time when the time module was initialized).
        import time
        print(time.time())
        # Output: 1602299933.233374
    
    2. time.sleep() - The time.sleep() function suspends the execution of the current thread for a specified number of seconds.
        time.sleep(2) #pause execution for 2 seconds
    
    3. time.strftime() - The time.strftime() function formats a time value as a string, based on a specified format. This function is particularly useful for formatting dates and times in a human-readable format, such as for display in a GUI, a log file, or a report. Here's an example:
        import time
        e=time.localtime
        print(time.strftime("%H:%M:%S",e()))
        print("done")
    
# Creating command line utility in python
Command line utilities are programs that can be run from the terminal or command line interface, and they are an essential part of many development workflows. In Python, you can create your own command line utilities using the built-in argparse module.
example program -
    import argparse
    import requests

    def download_img(url,output_name):
        img_data=requests.get(url)
        if img_data.status_code==200:
            with open(output_name,"wb") as file:
                file.write(img_data.content)
        else:
            print(img_data.status_code)

    parser=argparse.ArgumentParser(description="Download an image from a website")
    parser.add_argument("-url",required=True,help="Enter the url of the website")
    parser.add_argument("-o","--optional",type=str,help="Enter the optional argument")
    if parser.parse_args().optional is None:
        parser.parse_args().optional="output.jpg"
    args=parser.parse_args()
    download_img(args.url,args.optional)

## Walrus Operator 
In python earlier it was not possible to assign values in an expression but to fullfill this need walrus operator (:=) was introduced. We cannot do print(a=4) in python as this is not allowed but same thing can be done with walrus operator
```python
print(a:=4) #this will work because of walrus opeartor
```
Example-
```python
    fruits=list()
    while(fruit:=input("Enter a fruit: ")!="quit"):
        fruits.append(fruit)
    print(fruits)
````

## Shutil module
Used to perform high level file operation (built in module).The name "shutil" is short for shell utility. It provides a convenient and efficient way to automate tasks that are commonly performed on files and directories

### Common methods -
1. `shutil.copy(src, dst)`: This function copies the file located at src to a new location specified by dst. If the destination location already exists, the original file will be overwritten.

2. `shutil.copy2(src, dst)`: This function is similar to shutil.copy, but it also preserves more metadata about the original file, such as the timestamp.

3. `shutil.copytree(src, dst)`: This function recursively copies the directory located at src to a new location specified by dst. If the destination location already exists, the original directory will be merged with it.

4. `shutil.move(src, dst)`: This function moves the file located at src to a new location specified by dst. This function is equivalent to renaming a file in most cases.

5. `shutil.rmtree(path)`: This function recursively deletes the directory located at path, along with all of its contents. This function is similar to using the rm -rf command in a shell.

Example-
```python
    import shutil
    shutil.copytree("new folder","copied_folder")
    shutil.rmtree("copied_folder")
    shutil.copy("file1.txt","copied.txt")
    shutil.move("copied.txt","new folder")
```

## requests module
The Python Requests module is an HTTP library that enables developers to send HTTP requests in Python. This module enables you to send HTTP requests using Python code and makes it possible to interact with APIs and web services. To scrap webpages and to beautigy them we have to use bs4 module along with requests

Example (requests using simple post api)-
```python
    import requests
    url="https://jsonplaceholder.typicode.com/posts"
    headers={
        'Content-type': 'application/json; charset=UTF-8'
    }
    body={
        "title": 'chetan',
        "body": 'cyber-security',
        "userId": 1
    }
    send=requests.post(url,body,headers)
    print(send.text)
```

Example(using bs4 for scrapping)
```python
    from bs4 import BeautifulSoup
    import requests
    url="https://docs.python.org"
    r=requests.get(url)
    soup=BeautifulSoup(r.content,"html.parser")
    print(soup.prettify())
    for heading in soup.find_all("h1"):
        print(heading.text)
```

## generators in python
These are special type of function that allow to create an iterable sequence of values on the fly. This means generators doent store items in memory like list
it generates a value display it and frees the memory next time the new value is displayed and the process goes on

`yield` keyword is needed to return a value from the generator and suspends the execution of the program until a new value is requested
new value is requested by using the "next" keyword.

Example-
```python
    def generator():
        for i in range(300):
            yield i
    gen=generator()
    print(next(gen))
    print(next(gen))
```

## Function caching
Function caching can be implemented in python using the functools module. Function caching helps in the faster execution of a program. When a program is executed more than once with the same values as the module saves the result when the fucntion is executed with each argument and displays the result directly next time the function is called. The cache is only maintained in each run of the program and destroyed when the program gets executed. It is only ideal to use caching only when some functions which are necessary for the user needs to be cached as caching everything may increase the size of memory

Example-
```python
    from functools import lru_cache
    import time
    @lru_cache(maxsize=None)
    def count(n):
        time.sleep(n)
        return n*5
    print(count(3))
    print(count(1))
    print(count(3))
```

## Regular Expressions in Python
To use regular expression we need to import re module these regular expression with the help of meta characters help us to find complex sequences or words in strings

Example-
```python
    import re
    pattern=r"[A-Z]+elsh"
    text='''David Delsh (14 May 1944 17 July 2003) was a Welsh authority on biological warfare. Appointed to the United Nations Special Commission in 1991 as a chief weapons inspector in Iraq, he led ten of the organisations missions. After the publication of a dossier in 2002, which stated that Iraq could deploy chemical and biological weapons within 45 minutes, Kelly had an off-the-record interview with Andrew Gilligan of the BBC about the claim. Gilligans reporting stated that Alastair Campbell, the Downing Street director of communications, insisted on the 45-minute claim, something which Kelly denied saying. Kelly appeared before a parliamentary committee on 15 July 2003, and before another the next day; he was found dead near his home the day after. Tony Blair, the prime minister, set up an inquiry under Lord Hutton that concluded that Kelly had killed himself. A review led by Dominic Grieve between 2010 and 2011 backed the finding. Kellys death has been the subject of documentaries and been fictionalised in media works.'''
    print(re.findall(pattern,text))
```

## Async IO
In python generally functions execute one after another but if we want to run functions concurrently we can make function async. In Python, async programming is achieved through the use of the asyncio module and asynchronous functions.

Example-
```python
    import asyncio
    async def func1():
        print(1)
        await asyncio.sleep(2)
        return "func1"
    async def func2():
        print(2)
        await asyncio.sleep(3)
        return "func2"
    async def func3():
        print(3)
        await asyncio.sleep(2)
        return "func3"
    async def main():
        result=await asyncio.gather(func1(),func2(),func3()) #to run all the functions at the same time
        print(result)
    asyncio.run(main())
```

## Multithreading in Python
Multithreading is a technique in programming that allows multiple threads of execution to run concurrently within a single process. In Python, we can use the threading module to implement multithreading. We have to import threading module

Note - When we start a thread like `t1.start()` the computer just starts all the threads and moves to further lines of code for execution and the result will be given when they get completed to wait for the thread to complete before going further in the program we can use `threadname.join()`

Example-
```python
    import threading
    import time

    def func1(sec):
        print(f"sleeping for {sec} seconds")
        time.sleep(sec)
        print("done")
    #Normal code
    # func1(3)
    # func1(2)
    # func1(1)

    #Threading code
    t1=threading.Thread(target=func1,args=[3])
    t2=threading.Thread(target=func1,args=[2])
    t3=threading.Thread(target=func1,args=[1])

    t1.start()#start() will start the thread and move to the next line, rest of the code will be executed in parallel
    t1.join() #join() is used to wait for the thread to finish its task
    t2.start()
    t3.start()
    t2.join()
    t3.join()
```

We can also use ThreadPoolExecutor to ease the task of threading and can even use the map syntax to submit values in an iterable one by one
```python

    #Threading using ThreadPoolExecutor

    from concurrent.futures import ThreadPoolExecutor

    def func1(sec):
        print(f"sleeping for {sec} seconds")
        time.sleep(sec)
        print("done")
        return sec

    def poolingdemo():
        with ThreadPoolExecutor() as executor: # we can also do threading using ThreadPoolExecutor instead of threading.Thread
            future1=executor.submit(func1,3)
            future2=executor.submit(func1,2)
            future3=executor.submit(func1,1)
            print(future1.result())
            print(future2.result())
            print(future3.result())
            #Another syntax using map
            l=[5,4,3,2,1]
            results=executor.map(func1,l) #map will map the function to the list and execute it
            for result in results: #result here is the return value of the function
                print(result) 
    poolingdemo()
```

Note - Threading in Python allows you to run multiple tasks at the same time, giving the appearance of multitasking. Think of it like having multiple threads of execution, each doing its own thing. However, due to a limitation called the Global Interpreter Lock (GIL), threading in Python may not always provide true simultaneous execution for all tasks.

Asyncio, on the other hand, is a newer approach that helps you handle many tasks efficiently without the need for multiple threads. It works by using a special technique called coroutines and an event loop. Coroutines are like lightweight tasks that can pause and resume their execution, allowing other coroutines to run in the meantime. The event loop manages these coroutines, making sure they run smoothly.

## Multi-Processing
Multiprocessing allows you to run multiple processes simultaneously. Each process operates independently and has its own memory space. It enables true parallelism by utilizing multiple CPU cores. However, interprocess communication can be more complex and resource-intensive.

Threading, on the other hand, allows you to run multiple threads within a single process. Threads share the same memory space and can access shared data easily. However, due to the Global Interpreter Lock (GIL) in Python, which allows only one thread to execute Python bytecode at a time, threading may not provide true parallelism for CPU-bound tasks. It is better suited for I/O-bound tasks where threads can be blocked waiting for I/O operations.

1. The following are some of the most commonly used functions in the multiprocessing module:

    1.1 `multiprocessing.Process(target, args)`: This function creates a new process that runs the target function with the specified arguments.

    1.2 `multiprocessing.Pool(processes)`: This function creates a pool of worker processes that can be used to parallelize the execution of a function across multiple input values.

    1.3 `multiprocessing.Queue()`: This function creates a queue that can be used to communicate data between processes.

    1.4 `multiprocessing.Lock()`: This function creates a lock that can be used to synchronize access to shared resources between processes.

Example of program downloading multiple files by using multiple processes:
```PYTHON
    import multiprocessing
    import requests
    from concurrent.futures import ProcessPoolExecutor

    def downloadfile(url,name):
        print(f"started downloading {name}")
        response=requests.get(url)
        open(f"files/file{name}.jpg","wb").write(response.content)
        print(f"finished downloading {name}")

    if __name__=="__main__":
            url = "https://picsum.photos/2000/3000"
            pros=[]

            for i in range(0,5):                     
                downloadfile(url,i)
                p=multiprocessing.Process(target=downloadfile,args=[url,i])
                p.start()
                pros.append(p)
            for pro in pros:
                pro.join()
                      
                      #OR

            l1=[url for i in range(5)] #will print url 5 times
            l2=[i for i in range(5)]
            with ProcessPoolExecutor() as executor:
                results=executor.map(downloadfile,l1,l2)
                for r in results:
                        print(r)
```


