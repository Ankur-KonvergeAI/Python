## Program lines


```python
x = 2 # assignment statement; 2 is being asss=igned to variable x which is a memory location
x = x + 2 # assignment with expression
print(x) # print statement; print the value of x
```

    4
    

## Program flow

1. Sequence
2. Conditional
3. Repeated

## Variable Rules

1. Must start with letter or underscore(_) 
        teddy     
        teddy123    
        _teddy
2. Consist of letters, numbers and underscore(_)
        23teddy    
        *teddy     
        %teddy.123          (these are not allowed)
3. Case sensitive
        teddy    
        Teddy    
        TEDDY               (All valid variables)


```python
teddy = 2
Teddy = 22
print(teddy)
print(Teddy)
*teddy
print(*teddy)
```

    2
    22
    


      Input In [8]
        *teddy
        ^
    SyntaxError: can't use starred expression here
    


## Assignment statements


```python
x = 6
x = 3.9 * x * (1 - x)
print(x)
```

    -117.0
    



## Numeric expression
   


```python
#### Operator Precedence Rules
1. Parenthesis
2. Power
3. Multiplication
4. Addition
5. Left to right
```


```python
x = 1 + 2 * 3 - 4 / 5 ** 6
print(x)
```

    6.999744
    

## Type


```python
eee = 'hello' + 'there' # hello and there are string, since its inside single inverted comma
print(type(eee)) # print type of variable eee
```

    <class 'str'>
    


```python
eee = eee + 1 # string type is added with integer type
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Input In [17], in <cell line: 1>()
    ----> 1 eee = eee + 1
    

    TypeError: can only concatenate str (not "int") to str



```python
type(1)
```




    int




```python
print(type('hello'))
```

    <class 'str'>
    


```python
type(eee)
```




    str




```python
temp = 98.3
print(type(temp))
```

    <class 'float'>
    


```python
type(1.1)
```




    float




```python
print(10/2) # integer division produces floating result
```

    5.0
    

# # Type Conversion


```python
print(float(99)+100) # result of addition of float class with integer class is always float
```

    199.0
    


```python
i = 22
print(type(i))
print(float(i))
```

    <class 'int'>
    22.0
    


```python
i = 50
f = float(i)
print(type(f)) 
```

    <class 'float'>
    


```python
print(99/100) # division of interger produces floating class result
```

    0.99
    

# # String Conversion


```python
sval = '123'
print(type(sval)) # print type of variable sval
print(sval + 1) # print the output of sval(string) and 1(integer)
```

    <class 'str'>
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Input In [38], in <cell line: 3>()
          1 sval = '123'
          2 print(type(sval))
    ----> 3 print(sval + 1)
    

    TypeError: can only concatenate str (not "int") to str



```python
ival = int(sval)
print(type(ival))
```

    <class 'int'>
    


```python
nsv = 'hello bob'
niv = int(nsv)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    Input In [39], in <cell line: 2>()
          1 nsv = 'hello bob'
    ----> 2 niv = int(nsv)
    

    ValueError: invalid literal for int() with base 10: 'hello bob'


## User Inpur


```python
name = input("enter your name ") # input function return a string to variable name
print(name) # print the value in variable name
```

    enter your name Ankur
    Ankur
    


```python
name = input("enter your name ") # input function return a string to variable name
print("Welcome Mr. ", name) # print the value in variable name
```

    enter your name Ankur
    Welcom Mr.  Ankur
    

# Chapter 3: Conditional Execution


```python
x = 5
if x < 10:
    print('smaller')
if x > 20:
    print('bigger')
    
print('end the program')
```

    smaller
    end the program
    


```python
# Comparision Operator
x = 5
if x == 5:
    print("number equal to 5")
if x > 4:
    print("number is greater than 4")
if x >= 5:
    print("number is greater than or equal to 5")
if x < 6:
    print("number is less than 6")
if x != 5:
    print("number not equal to 6")
```

    number equal to 5
    number is greater than 4
    number is greater than or equal to 5
    number is less than 6
    


```python
#one way decision
x = 5
print ('Before 5')
if x==5:
    print('is 5')
    print('is still 5')
    print('...still 5')
print('Afterwards 5')
print ('Before 6')
if x==6:
    print('is 6')           # not executed
    print('is still 6')     # not executed
    print('...still 6')     # not executed
print('Afterwards 6')
```

    Before 5
    is 5
    is still 5
    ...still 5
    Afterwards 5
    Before 6
    Afterwards 6
    


```python
# Nested decision

x = 42
if x > 1:
    print('more than one')
    if x < 100:
        print('less than hundred')
print('done')
```

    more than one
    less than hundred
    done
    


```python
x = 142
if x > 1:
    print('more than one')
    if x < 100:
        print('less than hundred')
print('done')
```

    more than one
    done
    


```python
x = -142
if x > 1:
    print('more than one')
    if x < 100:
        print('less than hundred')
print('done')
```

    done
    


```python
# Two way decision

x = 4
if x > 2:
    print('big')
else:
    print('small')

print("done printing")
    
```

    big
    done printing
    


```python
# Multiway

x = 4
if x < 2:
    print('small')
elif x < 10:
    print('medium')
else:
    print('large')
print('all done')
    
```

    medium
    all done
    


```python
x = 1
if x < 2:
    print('small')
elif x < 10:
    print('medium')
else:
    print('large')
print('all done')
```

    small
    all done
    


```python
x = 40
if x < 2:
    print('small')
elif x < 10:
    print('medium')
else:
    print('large')
print('all done')
```

    large
    all done
    

## Try and accept
When try instruction fails, except instruction gets executed. 
program does not get stuck in between and continues


```python
astr = 'Hello Bob'
try:
    istr = int(astr)
except:
    istr = -1
    
print(istr)
```

    -1
    


```python
astr = '1234'
try:
    istr = int(astr)
except:
    istr = -1
    
print(istr)
```

    1234
    


```python
astr = "bob"
try:
    print('hello')
    istr = int(astr)
    print('there')
except:
    istr = -1

print(istr)
```

    hello
    -1
    


```python
rawstr = input("enter a number: ")
try:
    ival = int(rawstr)
except:
    ival = -1
    
if ival > 0:
    print('nice work')
else:
    print('not a number')
```

    enter a number: 56
    nice work
    


```python
rawstr = input("enter a number: ")
try:
    ival = int(rawstr)
except:
    ival = -1
    
if ival > 0:
    print('nice work')
else:
    print('not a number')
```

    enter a number: two
    not a number
    

## Chapter 4: Functions


```python
x = 5
print ('Hello')

def print_lyrics():            # just defining funcyion, but not calling
    print("I'am a lumberjack")
    print("I sleep all night")

print("Yo")
print_lyrics()
x = x + 2
print(x)
    
```

    Hello
    Yo
    I'am a lumberjack
    I sleep all night
    7
    


```python
# Argument passing

def greet(lang):
    if lang=='es':
        print('Hola')
    elif lang=='fr':
        print('Bonjour')
    else:
        print('Hello')
        
greet('en')
```

    Hello
    


```python
def greet(lang):
    if lang=='es':
        print('Hola')
    elif lang=='fr':
        print('Bonjour')
    else:
        print('Hello')
        
greet('es')
```

    Hola
    


```python
# Return Value

def greet():
    return "Hello"

print(greet(), "Glenn")
print(greet(), "Sally")
```

    Hello Glenn
    Hello Sally
    


```python
def greet(lang):
    if lang=='es':
        return 'Hola'
    elif lang=='fr':
        return 'Bonjour'
    else:
        return 'Hello'
        
print(greet('fr'), "Glenn")
```

    Bonjour Glenn
    


```python
def greet(lang):
    if lang=='es':
        return 'Hola'
    elif lang=='fr':
        return 'Bonjour'
    else:
        return 'Hello'
        
print(greet('qq'), "Glenn")
```

    Hello Glenn
    


```python
# Multiple parameter/arguments

def addtwo(a, b):
    added = a + b
    return added

x = addtwo(3,5)
print(x)
```

    8
    


```python
def addtwo(a, b):
    added = a + b
    return             #no value is being returned    

x = addtwo(3,5)
print(x)
```

    None
    

# Chapter 5: Loop and iteration


```python
# while loop

n = 5
while n > 0:
    print(n)
    n = n-1
print("blastoff")
print(n) 
```

    5
    4
    3
    2
    1
    blastoff
    0
    


```python
# Breaking out of loop

while True:
    line = input('who are you ')
    if line == 'done':
        break
    print(line)
print('Done')
```

    who are you g
    g
    who are you u
    u
    who are you 6
    6
    who are you 6
    6
    who are you done
    Done
    


```python
while True:
    line = input('who are you ')
    if line == 'done':
        break
    print(line)
print('Done')
```

    who are you done
    Done
    


```python
# continue

while True:
    line = input('who are you ')
    if line == '#':
        continue
    if line == 'done':
        break
    print(line)
print('Done')
```

    who are you #
    who are you done
    Done
    

### Definite loops


```python
# For loop

for i in [5,4,3,2,1]:
    print(i)
print("blastoff")
```

    5
    4
    3
    2
    1
    blastoff
    


```python
friends = ["Joseph", "Glenn", "Sally"]
for friend in friends:
    print('Happy New Year', friend)
print('Done!')
```

    Happy New Year Joseph
    Happy New Year Glenn
    Happy New Year Sally
    Done!
    


```python
# Loop Idioms

print('before')
for thing in [6, 9, 11, 16, 17]:
    print(thing)
print('after')
```

    before
    6
    9
    11
    16
    17
    after
    


```python
# finding the largest number

initial = -1
print('before', initial)
for num in [8,41,12,3,74,15]:
    if num > initial:
        initial = num
    print(initial)
print('After', initial)   
```

    before -1
    8
    41
    41
    41
    74
    74
    After 74
    


```python
# Finding the average in a loop

count = 0
sum = 0
print('before', count, sum)
for value in [9,41,12,3,74,15]:
    count = count + 1
    sum = sum + value
    print(count, sum, value)
print('After', count, sum, sum/count)
```

    before 0 0
    1 9 9
    2 50 41
    3 62 12
    4 65 3
    5 139 74
    6 154 15
    After 6 154 25.666666666666668
    


```python
# search using boolean variable

found = False
print('Before', found)
for value in [9,41,12,3,74,15]:
    if value == 3:
        found = True
    print(found, value)
print('After', found)
```

    Before False
    False 9
    False 41
    False 12
    True 3
    True 74
    True 15
    After True
    


```python
# find the smallest value

smallest_so_far = -1
print('Before', smallest_so_far)
for num in [9,41,12,3,74,15]:
    if num < smallest_so_far:
        smallest_so_far = num
    print(smallest_so_far, num)
print('After', smallest_so_far)
```

    Before -1
    -1 9
    -1 41
    -1 12
    -1 3
    -1 74
    -1 15
    After -1
    


```python
smallest = None
print('Before')
for value in [9,41,12,3,74,15]:
    if smallest is None:
        smallest = value
    elif value < smallest:
        smallest= value
    print(smallest, value)
print('After', smallest)
```

    Before
    9 9
    9 41
    9 12
    3 3
    3 74
    3 15
    After 3
    


```python

```

# Chapter 6: Strings


```python
fruit = "banana"
letter = fruit[0]
print(letter)
```

    b
    


```python
fruit = "banaxa"
x= 3
w = fruit[x-1]
print(w)
```

    n
    


```python
zot = 'abc'
print(zot[5])
```


    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    Input In [22], in <cell line: 2>()
          1 zot = 'abc'
    ----> 2 print(zot[5])
    

    IndexError: string index out of range



```python
fruit = "banana"
print(len(fruit))
```

    6
    


```python
index = 0
while index < len(fruit):
    letter = fruit[index]
    print(letter)
    index = index + 1
```

    b
    a
    n
    a
    n
    a
    


```python
word = 'banana'
count = 0 
for letter in word:
    if letter == 'a':
        count = count + 1
    print(count)
```

    0
    1
    1
    2
    2
    3
    


```python
# Slicing Strings

s = 'Money Python'
print(s[0:4])
```

    Mone
    


```python
s = 'Money Python'
print(s[:3])
```

    Mon
    


```python
s = 'Money Python'
print(s[8:])
```

    thon
    


```python
s = 'Money Python'
print(s[:])
```

    Money Python
    


```python
# String Concatenation

a = 'Hello'
b = a + 'There'
print(b)
```

    HelloThere
    


```python
a = 'Hello'
b = a + ' ' + 'There'
print(b)
```

    Hello There
    


```python
# 'in' as a logical operator

fruit = 'banana'
"m" in fruit
```




    False




```python
fruit = 'banana'
'n' in fruit
```




    True




```python
fruit = 'banana'
if 'a' in fruit:
    print('found it')
```

    found it
    


```python
# String Library

greet = 'HELLO BOB'
zap = greet.lower()
print(zap)
print(greet)
print('Hi There'.lower())
```

    hello bob
    HELLO BOB
    hi there
    


```python
stuff = "hello there"
type(stuff)
dir(stuff)
```




    ['__add__',
     '__class__',
     '__contains__',
     '__delattr__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getitem__',
     '__getnewargs__',
     '__gt__',
     '__hash__',
     '__init__',
     '__init_subclass__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__mod__',
     '__mul__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__rmod__',
     '__rmul__',
     '__setattr__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'capitalize',
     'casefold',
     'center',
     'count',
     'encode',
     'endswith',
     'expandtabs',
     'find',
     'format',
     'format_map',
     'index',
     'isalnum',
     'isalpha',
     'isascii',
     'isdecimal',
     'isdigit',
     'isidentifier',
     'islower',
     'isnumeric',
     'isprintable',
     'isspace',
     'istitle',
     'isupper',
     'join',
     'ljust',
     'lower',
     'lstrip',
     'maketrans',
     'partition',
     'removeprefix',
     'removesuffix',
     'replace',
     'rfind',
     'rindex',
     'rjust',
     'rpartition',
     'rsplit',
     'rstrip',
     'split',
     'splitlines',
     'startswith',
     'strip',
     'swapcase',
     'title',
     'translate',
     'upper',
     'zfill']




```python

```
