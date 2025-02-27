# Functions

### Types Built- In function categories
Type conversion Functions
Input and Output Functions
Mathematical Functions
Iterables and Sequences Function
File Handling Functions
Miscellaneous Functions
### Example


```python
#defining a function
def greet():
    print("Hello")
#calling the function
greet()
```

    Hello
    


```python
#type conversion functions
int("10")        #converts string to integer -->10
float("3.14")    #converts string to float --> 3.14
str(100)         #converts integer to string --> '100'
bool(0)          #converts to boolean (False)
list("abc")      #converts string to list --> ['a','b','c']
tuple([1,2,3])   #converts list to tuple --> (1,2,3)
set([1,2,2])     #converts list to set --> {1,2}
dict([(1,'one'),(2,'two')]) #converts list of tuples to dictionary
```




    {1: 'one', 2: 'two'}




```python
#convert string '100' to integer
int('100')
```




    100




```python
#convert the float 3.14 to integer
int(3.14)
```




    3




```python
#convert the number 25 into a string
str(25)
```




    '25'




```python
#convert the list [1,2,3] into a tuple
tuple([1,2,3])
```




    (1, 2, 3)




```python
#convert the tuple (4,5,6) into a list.
list((4,5,6))
```




    [4, 5, 6]




```python
#input and output functions
input("Enter your name")
print("HEllo")
```

    Enter your name Pranav
    

    HEllo
    


```python
#write a program that takes user name as input and prints "Hello, <name> !"
x = input("Enter the name : ")
print(f"Hello {x} !")
```

    Enter the name :  Pranav
    

    Hello Pranav !
    


```python
#Print "Python is fun !" using print()
print('Python is fun !')
```

    Python is fun !
    


```python
#take two nos as input and print their sum.
a = int(input("Enter no 1: "))
b = int(input("Enter no 2: "))
c = a+b
print(f"Sum is {c}.")
```

    Enter no 1:  2
    Enter no 2:  3
    

    Sum is 5.
    


```python
#take a sentence as input and print its length
string = input('Enter the string: ')
print(f'The length of the string is {len(string)}.')
```

    Enter the string:  Hi I am Pranav.
    

    The length of the string is 15.
    


```python
#Take a user's birth year as input and print their age
year = int(input("Enter the birth year : "))
current_age = 2025 - year
print(f"Current age is {current_age}.")
```

    Enter the birth year :  1999
    

    Current age is 26.
    


```python
#Take a user's birth year as input and print their age using datetime
from datetime import datetime
year_1 = int(input("Enter the birth year : "))
current_age_1 = datetime.now().year - year_1
print(f"Current age is {current_age_1}.")
```

    Enter the birth year :  1999
    

    Current age is 26.
    


```python
#mathematical functions
abs(-5)      #Returns absolute value -->
pow(2,3)     #2^3 -->8
round(3.7)   #Rounds to nearest integer --> 4
divmod(10,3) #Returns quotient and remainder -->(3,1)
```




    (3, 1)




```python
#find the absolute value of -15
abs(-15)
```




    15




```python
#Compute 2^5 using pow()
pow(2,5)
```




    32




```python
#round 4.6 to the nearest integer
round(4.6)
```




    5




```python
#Find the quotient and remainder when dividing 19 by 4
divmod(19,4)
```




    (4, 3)




```python
#calculate the sum of numbers in [10,20,30]
sum([10,20,30])
```




    60




```python
#iterables and sequences functions
len([1,2,3])           #retruns length -->3
max(4,7,2)             #returns max value -->7
min([10,20,30])        #returns min value -->10
sum([1,2,3])           #returns sum -->6
sorted([3,1,2])        #sorts list -->[1,2,3]
sorted([3,1,2],reverse = True) #sorts list --> [3,2,1]
range(5)               #Generates sequence --> 0,1,2,3,4
```




    range(0, 5)




```python
#find the length of the list
list_1 = [5,10,15]
print(f'the length is {len(list_1)}')
```

    the length is 3
    


```python
#find the maximum number in [12,7,19,3]
print(f"the maximum number in [12,7,19,3] is {max([12,7,19,3])}")
```

    the maximum number in [12,7,19,3] is 19
    


```python
#Find the minimum number in [12,7,19,3]
print(f"the minimum number in [12,7,19,3] is {min([12,7,19,3])}")
```

    the minimum number in [12,7,19,3] is 3
    


```python
#sort the list [8,2,5,1]
print(sorted([8,2,5,1]))
```

    [1, 2, 5, 8]
    


```python
#Generate a sequence of numbers 1 to 5 using range().
for i in range(1,6):
    print(i,end = ' ')
```

    1 2 3 4 5 


```python
#object and memory functions
type(10)            #returns type--> <class 'int'>
id(10)              #returns memory address
isinstance(10,int)  #Checks if object is of a type -->True
dir(list_name)      # find all available methods for the list datatype
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[14], line 5
          3 id(10)              #returns memory address
          4 isinstance(10,int)  #Checks if object is of a type -->True
    ----> 5 dir(list_name)      # find all available methods for the list datatype
    

    NameError: name 'list_name' is not defined



```python
#Find the type of "Hello"
print(f'The type of \'Hello\' is {type("Hello")}.')
```

    The type of 'Hello' is <class 'str'>.
    


```python
#Get the memory address of variable x = 42
x = 42
print(f'the memory address of x is {id(x)}.')
```

    the memory address of x is 140708962175176.
    


```python
#Check if 7 is an integer
isinstance(7,int)
```




    True




```python
#check if 3.14 is a float
isinstance(3.14,float)
```




    True




```python
#find all available methods for list
example_list = []
dir(example_list)
```




    ['__add__',
     '__class__',
     '__class_getitem__',
     '__contains__',
     '__delattr__',
     '__delitem__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getitem__',
     '__getstate__',
     '__gt__',
     '__hash__',
     '__iadd__',
     '__imul__',
     '__init__',
     '__init_subclass__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__mul__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__reversed__',
     '__rmul__',
     '__setattr__',
     '__setitem__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'append',
     'clear',
     'copy',
     'count',
     'extend',
     'index',
     'insert',
     'pop',
     'remove',
     'reverse',
     'sort']




```python
#file handling functions
#open('file.txt', 'r') #opens file in read mode however we need to close the file after use.
x = 10
with open('sample.txt','w') as f:
    f.write('Hello, World\n') #automatically closes file after use --> with
    f.write('World Hello\n')
    f.write(f'abcdef\naadarsh\npranav\n {x}')
```


```python
with open('sample.txt','r') as f:
    file = f.read() #automatically closes file after use --> with
print(file)
```

    Hello, World
    World Hello
    abcdef
    aadarsh
    pranav
     10
    


```python
def greet(name = 'Guest'): #default value is set to Guest if no name is set.
    print(f"Welcome {name}!")
name = input("Enter your name: ")
greet(name)
```

    Enter your name:  
    

    Welcome !
    


```python
def add_nos(a,b):
    return sum([a,b])
sum_ = add_nos(int(input("Enter 1st no: ")),int(input("Enter 2nd no: ")))
print(sum_)
```

    Enter 1st no:  2
    Enter 2nd no:  3
    

    5
    


```python
def multiply(a=1,b=1):
    c = a*b
    return c
product = multiply(int(input("Enter 1st no: ")),int(input("Enter 2nd no: ")))
print(product)
```

    Enter 1st no:  2
    Enter 2nd no:  3
    

    6
    


```python
def arith_ops(a,b):
    '''this function adds, multiplies,subtracts and divides'''
    return sum([a,b]),a-b,a*b,a/b
add,diff,mul,div = arith_ops(int(input("Enter 1st: ")),int(input("Enter 2nd: ")))
print(f"sum is {add} ,difference is {diff} ,product is {mul} ,division is {div:.2f}.")
    
    
```

    Enter 1st:  3
    Enter 2nd:  2
    

    sum is 5 ,difference is 1 ,product is 6 ,division is 1.50.
    


```python
print(arith_ops.__doc__)
```

    this function adds, multiplies,subtracts and divides
    

#scope
#### Local Scope : variable exists inside a function
#### Global Scope : variable exists outside all functions
#### Example


```python
x = 10 #Global variable
def my_func():
    #x = 5 #Local variable
    global x # accessing global x in local space
    x +=1 

    print("Inside function:", x)
my_func()
print("outside function:", x)
```

    Inside function: 11
    outside function: 11
    

#### docstring


```python
print(list.append.__doc__) # accessing docstring of a function
```

    Append object to the end of the list.
    

#### Keyword arguments
Can handle any number of inputs.


```python
def print_info(*kwargs): #kwargs is standard ,can use any variable with *
    for item in kwargs:
        print(item, end =' ')
print_info('hi',10,'bye')
```

    hi 10 bye 


```python

```
