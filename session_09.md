# Python OOP Concept

Object  
Class  
Inheritance  
Encapsulation   
Polymorphism  

Class - structure which can hold data and functions, a hollow structure  
Object - collection of data and methods which operate on data.  


```python
class Person:
    def __init__(self,name,age): #--> constructor
        self.name = name
        self.age = age

    def sayHello(self):
        print(self.name) #--> self is p1 when called so self.name is p1.name.

p1 = Person("Dan", 1234) #--> object
p1.sayHello() #--> when it is called it is changed to self.sayHello.

#self denotes p1 itself.
    
```

    Dan
    


```python
class Pet:
    def __init__(self, name, age, sound):
        self.name = name
        self.age = age
        self.sound = sound
    def say(self):
        print(self.sound)
```


```python
my_pet = Pet("Bob",5,"Woof!!") # object created with class Pet
```


```python
print(my_pet.name)
print(my_pet.age)
print(my_pet.sound *2)
my_pet.say()
```

    Bob
    5
    Woof!!Woof!!
    Woof!!
    


```python
my_pet2 = Pet("Tuftee", 2, "Meawww!!") #object created with class Pet
print(my_pet2.name, my_pet2.age, sep = '  ')
```

    Tuftee  2
    


```python
my_pet2.say()
```

    Meawww!!
    


```python
class Animal:
    def __init__(self,name,age,sound):
        self.name = name
        self.age = age
        self.sound = sound
    def make_sound(self):
        print(self.sound*3)
```


```python
class Dog(Animal):
    def __init__(self,name,age,sound,color):
        super().__init__(name,age,sound) # this is done so that we need not initialize all attributes again
        self.color = color #if we are adding a new attribute in child clss we need to initilize it again. 
    def action(self):
        print("Moves tails")
```


```python
# class Cat(Animal):
#     def __init__(self,name,age):
#         super().__init__(name,age,"Meawww!!")
#     def action(self):
#         print("Moves ears")
```


```python
dog_1 = Dog("Piku",2, "bowbow","black")
```


```python
print(dog_1.sound)
print(dog_1.color)
```

    bowbow
    black
    


```python
dog_1.make_sound()
```

    bowbowbowbowbowbow
    

## Abstract Class


```python
# from abc import ABC,abstractmethod

# class Dog(ABC): # abstract class
#     def __init__(self,name):
#         self.name = name
        
#     @abstractmethod
    
```


```python
def will_define_later():
    pass # use this and we can define function later. pass will sit as a place holder and prevent error
```

#### Define a class Calculator which has two attributes and do arithmetic operations , addition, subtraction, multiplications and division.


```python
class Calculator:
    def __init__(self,num_1 = 1,num_2 = 1):
        self.num_1 = num_1
        self.num_2 = num_2
    def add(self):
        sum = self.num_1 + self.num_2
        return sum
    def sub(self):
        diff = self.num_1 - self.num_2
        return diff
    def product(self):
        prod = self.num_1 * self.num_2
        return prod
    def div(self):
        quotient,remainder = divmod(self.num_1,self.num_2)
        return quotient,remainder
```


```python
calculate = Calculator(int(input("Enter number 1: ")), int(input("Enter number 2: ")))
print(f"\nThe sum is {calculate.add()}.")
print(f"The difference is {calculate.sub()}.")
print(f"The product is {calculate.product()}.")
q,d = calculate.div()
print(f"The quotient is {q} and remainder is {d}.")
```

    Enter number 1:  10
    Enter number 2:  2
    

    
    The sum is 12.
    The difference is 8.
    The product is 20.
    The quotient is 5 and remainder is 0.
    

# List all PDF files in the download directory


```python
#Method _1
from os import listdir
file_names = listdir(r"C:\Users\prana\Downloads")
for i in file_names:
    if '.pdf' in i:
        print(i)
```

    KEY_Responses_Rank_List_and_Analysis.pdf
    


```python
#Method_2
from os import listdir
from os import path
from os.path import getsize
file_path = path.join("C:","Users","prana","Downloads")
file_names_1 = listdir(file_path)
for i in file_names_1:
    if '.pdf' in i:
        print(i)

```

    Excel and Cognos -1.pdf
    Excel and Cognos -2.pdf
    Excel and Cognos -3.pdf
    Excel shortcuts.pdf
    KEY_Responses_Rank_List_and_Analysis.pdf
    

#### getting size of a file


```python
for name in file_names_1:
    name = path.join("C:","Users","prana","Downloads",name)
    file_size = getsize(name)
    print(f'filename \'{name}\' has size {file_size} KB\'s')
```

    filename 'C:Users\prana\Downloads\desktop.ini' has size 282 KB's
    filename 'C:Users\prana\Downloads\Excel and Cognos -1.pdf' has size 879467 KB's
    filename 'C:Users\prana\Downloads\Excel and Cognos -2.pdf' has size 647911 KB's
    filename 'C:Users\prana\Downloads\Excel and Cognos -3.pdf' has size 856891 KB's
    filename 'C:Users\prana\Downloads\Excel shortcuts.pdf' has size 311944 KB's
    filename 'C:Users\prana\Downloads\indian_startup_funding_Lab1.xlsx' has size 21320 KB's
    filename 'C:Users\prana\Downloads\indian_startup_funding_Lab3.xlsx' has size 22994 KB's
    filename 'C:Users\prana\Downloads\indian_startup_funding_Lab6.xlsx' has size 23723 KB's
    filename 'C:Users\prana\Downloads\indian_startup_funding_Lab7.xlsx' has size 23818 KB's
    filename 'C:Users\prana\Downloads\KEY_Responses_Rank_List_and_Analysis.pdf' has size 51719 KB's
    

#### file with max file_size


```python
max_dict = {}
for name in file_names_1:
    name = path.join("C:","Users","prana","Downloads",name)
    file_size = getsize(name)
    max_dict[file_size] = name
    
print(f'filename \'{max_dict[max(max_dict.keys())]}\' has  maximum size of {max(max_dict.keys())} KB\'s')
```

    filename 'C:Users\prana\Downloads\Excel and Cognos -1.pdf' has  maximum size of 879467 KB's
    

# Python Practice Problems


1. Data Types and Operators
- Write a program to add two integers.
- Write a program to subtract two floats.
- Write a program to multiply two numbers.
- Write a program to divide two numbers and handle division by zero.
- Write a program to find the remainder of two numbers using the modulus operator.
- Write a program to swap two variables without using a third variable.
- Write a program to check if a number is even or odd.
- Write a program to find the square of a number.
- Write a program to find the cube of a number.
- Write a program to convert Celsius to Fahrenheit.

2. String Handling
- Write a program to concatenate two strings.
- Write a program to find the length of a string.
- Write a program to reverse a string.
- Write a program to check if a string is a palindrome.
- Write a program to count the number of vowels in a string.
- Write a program to convert a string to uppercase.
- Write a program to convert a string to lowercase.
- Write a program to replace a substring in a string.
- Write a program to check if a string starts with a specific prefix.
- Write a program to check if a string ends with a specific suffix.

3. Conditional Statements
- Write a program to find the largest of three numbers.
- Write a program to check if a number is positive, negative, or zero.
- Write a program to check if a year is a leap year.
- Write a program to check if a number is divisible by both 3 and 5.
- Write a program to check if a character is a vowel or consonant.
- Write a program to check if a number is within a given range.
- Write a program to compare two strings and print the larger one.
- Write a program to calculate the grade based on a student's score.
- Write a program to check if a number is a prime number.

4. Loops
- Write a program to print numbers from 1 to 10 using a for loop.
- Write a program to print numbers from 10 to 1 using a while loop.
- Write a program to print the multiplication table of a number.
- Write a program to find the sum of all numbers from 1 to 100.
- Write a program to find the factorial of a number.
- Write a program to print all even numbers between 1 and 50.
- Write a program to print the Fibonacci series up to n terms.
- Write a program to check if a number is an Armstrong number.
- Write a program to print the following pattern:
*
**
***
****
*****

- Write a program to find the sum of digits of a number.

5. Functions
- Write a function to add two numbers.
- Write a function to find the maximum of two numbers.
- Write a function to check if a number is prime.
- Write a function to reverse a string.
- Write a function to calculate the factorial of a number.
- Write a function to check if a string is a palindrome.
- Write a function to find the area of a circle.
- Write a function to find the GCD of two numbers.
- Write a function to find the LCM of two numbers.
- Write a function to print the first n terms of the Fibonacci series.

6. Lists
- Write a program to find the sum of all elements in a list.
- Write a program to find the largest element in a list.
- Write a program to find the smallest element in a list.
- Write a program to reverse a list.
- Write a program to count the occurrences of an element in a list.
- Write a program to remove duplicates from a list.
- Write a program to check if a list is sorted.
- Write a program to merge two lists.
- Write a program to find the second largest element in a list.
- Write a program to sort a list in ascending order.

7. Tuples
- Write a program to create a tuple and print its elements.
- Write a program to find the length of a tuple.
- Write a program to concatenate two tuples.
- Write a program to check if an element exists in a tuple.
- Write a program to find the index of an element in a tuple.
- Write a program to count the occurrences of an element in a tuple.
- Write a program to convert a tuple to a list.
- Write a program to reverse a tuple.
- Write a program to find the maximum element in a tuple.
- Write a program to find the minimum element in a tuple.

8. Dictionaries
- Write a program to create a dictionary and print its keys and values.
- Write a program to add a new key-value pair to a dictionary.
- Write a program to remove a key from a dictionary.
- Write a program to check if a key exists in a dictionary.
- Write a program to find the length of a dictionary.
- Write a program to merge two dictionaries.
- Write a program to find the sum of all values in a dictionary.
- Write a program to sort a dictionary by its keys.
- Write a program to sort a dictionary by its values.
- Write a program to find the key with the maximum value in a dictionary.

9. Sets
- Write a program to create a set and add elements to it.
- Write a program to remove an element from a set.
- Write a program to find the union of two sets.
- Write a program to find the intersection of two sets.
- Write a program to find the difference between two sets.
- Write a program to check if a set is a subset of another set.
- Write a program to check if two sets are disjoint.
- Write a program to find the length of a set.
- Write a program to clear all elements from a set.
- Write a program to convert a list to a set.

10. Basics of OOPs
- Write a class to represent a Rectangle with methods to calculate area and perimeter.
- Write a class to represent a Circle with methods to calculate area and circumference.
- Write a class to represent a Student with attributes like name, roll number, and marks.
- Write a class to represent a BankAccount with methods to deposit and withdraw money.
- Write a class to represent a Car with attributes like make, model, and year.
- Write a class to represent a Book with attributes like title, author, and price.
- Write a class to represent a Person with attributes like name and age, and a method to display details.
- Write a class to represent a Bank with methods to add accounts and display total balance.
- Write a class to represent a Shape with a method to calculate area, and create subclasses for Square and Circle.

```python

```
