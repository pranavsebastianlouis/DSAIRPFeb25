```python
x = 10
if x > 5:
    print("x is greater than 5.")
    print("x contains :", x )
else:
    print("x is less than 5.")

```

    x is greater than 5.
    


```python
x = 1
if x:
    print("x is not zero")
else :
    print("x is 0 or False or None")
```

    x is not zero
    


```python
x = 7
if x > 5:
    print("x is greater than 5.")
    print(list(range(x)))
else:
    print("x is not greater than 5.")
```

    x is greater than 5.
    [0, 1, 2, 3, 4, 5, 6]
    


```python
x = 10
if x > 10:
    print("x is greater than 10.")
elif x == 10:
    print("x is exactly 10.")
```

    x is exactly 10.
    


```python
x = int(input("Enter the number: "))
if x > 0:
    print("number is positive")
elif x == 0:
    print ("number is zero")
elif x < 0:
    print("number is negative")
```

    Enter the number:  -1
    

    number is negative
    


```python
x = input("Enter the number : ")
name = ''
num_dict = {'1':'One','2':'Two','3':'Three','4':'Four','5':'Five','6':'Six','7':'Seven','8':'Eight','9':'Nine'}
for char in x:
    name = name + num_dict[char] + ' '
print(name)
    
```

    Enter the number :  1234
    

    One Two Three Four 
    


```python
x = 15
if x>10 and x>20:
    print("x is greater than 10 and 20")
```


```python
string = input("Enter the string: ")
if string.lower() == string[::-1].lower():
    print("Palindrome")
else:
    print("Not Palindrome")
```

    Enter the string:  Malayalam
    

    Palindrome
    


```python
#check a given number is divisible by 9 if it is odd and divisible by 4 if it is even
num = int(input("Enter a number: "))
if (num%2 != 0) and (num%9 == 0):
    print("number is divisible by 9")
elif (num%2 == 0) and (num%4 == 0):
    print("number is divisible by 4")
```

    Enter a number:  8
    

    number is divisible by 4
    


```python
 number = int(input("Enter the number: "))
if number < 60:
    print('F')
elif (number >= 60) and (number <= 69):
    print("D")
elif (number >= 70) and (number <= 79):
    print("C")
elif (number >= 80) and (number <= 89):
    print("B")
elif number >= 90:
    print("A")
```

    Enter the number:  69
    

    D
    


```python
import keyword
print(keyword.kwlist)
print(len(keyword.kwlist))
```

    ['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
    35
    


```python
''' aaaaa
aaaaa
aaa '''
```




    ' aaaaa\naaaaa\naaa '




```python
1+2+\
4+5\
+6
```




    18




```python
name, age = 'Bob', 23
print(name,age)
```

    Bob 23
    


```python
print('{} is {} years old.'.format(name,age))
print(f"{name} is {age} years old.")
```

    Bob is 23 years old.
    Bob is 23 years old.
    


```python
word = 'data'
for char in word[::-1]:
    print(char)
```

    a
    t
    a
    d
    


```python
numbers = [1,2,3,4,5]
for i in numbers:
    if i == 3:
        break
    print(i)
print("outside of for loop")
```

    1
    2
    outside of for loop
    


```python
numbers = [1,2,3,4,5]
for i in numbers:
    if i == 3:
        continue
    print(i)
print("outside of for loop")
```

    1
    2
    4
    5
    outside of for loop
    


```python
"Hello "*3
```




    'Hello Hello Hello '




```python
x = int(input("Enter : "))
for i in range(1,x+1):
    print("*"*i)
```

    Enter :  5
    

    *
    **
    ***
    ****
    *****
    


```python
n = int(input("Enter the number of rows: "))
for i in range(1,n,2):
    nsp = (n-i)//2
    print(" "*nsp + "*"*i + " "*nsp)

```

    Enter the number of rows:  20
    

             *         
            ***        
           *****       
          *******      
         *********     
        ***********    
       *************   
      ***************  
     ***************** 
    *******************
    


```python
n = int(input("Enter no of rows: "))
for i in range(0,n+1):
    print(" "*(n-i) + '*'*i)
```

    Enter no of rows:  5
    

         
        *
       **
      ***
     ****
    *****
    


```python
n = int(input("Enter the number of rows: "))
for i in range(n,-1,-2):
    nsp = (n-i)//2
    print(" "*nsp + "*"*i + " "*nsp)
```

    Enter the number of rows:  21
    

    *********************
     ******************* 
      *****************  
       ***************   
        *************    
         ***********     
          *********      
           *******       
            *****        
             ***         
              *          
    


```python
n = 1
while n<10:
    print(n)
    n = n+1
    
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    


```python

```
