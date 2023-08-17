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

#Operators
Operators are symbols in python used to perform some specific operation
Types of builtin operators-
    +   -   add
    -   -   subtraction
    *   -   multiplication
    **  -   exponential
    /   -   division (returns quotient)
    %   -   modulus (returns remainder)
    //  -   floor division (returns quotient as whole number)

#Typecasting in Python
The conversion of one datatype into another datatype is what we refer to as Typecasting
Python supports plenty of functions for performing typecasting like int(), float(), str(), ord(), hex(), oct(), tuple(), set(), list(), dict(), etc

There are two type of typecasting -
    1.Explicit Conversion (Explicit type casting in python) - This is done by the programmer manually as per requirement it is achieved by using functions like int(),float() etc.
            a="9"
            b="7"
            print(a+b) # this will show 97 as output
            print(int(a)+int(b)) # this will show 16 as output because of type casting

    2.Implicit Conversion (Implicit type casting in python) -   Datatypes in python do not have same order. So when an operation is performed
    between two different datatypes the python interpreter automatically converts the smaller datatype to the higher datatype to prevent data loss
    this is called implicit conversion or typecasting.
        a=9.9
        b=7
        print(a+b)  # this will show 16.9 as output because of implicit type casting

#Taking user input in python
    We can taker user input in python with the help of input() function. It generally returns value as string or character.
    But input function returns the value as string. Hence we have to typecast them whenever required to another datatype.
    We can also display a text using input function. This will make input() function take user input and display a message as well.
        a=int(input("Enter a number: "))  #typecasting as int() in input as well as displaying message

#Strings
In python, anything that you enclose between single or double quotation marks is considered a string. A string is essentially a sequence or array of textual data. Strings are used when working with Unicode characters.
    eg- "Chetan"
It doesnt matter if you use single quotation marks or double quotation marks while making a string.
If you want to use (" or ') inside a string you can use escape sequence characters like /" or /' or you can enclose single quotation marks inside double quotationmark string and vice versa
    eg - print("hello 'chetan'") or print ("hello /'chetan/'")

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



