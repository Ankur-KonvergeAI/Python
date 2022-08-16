# Opening a file


```python
fhand= open('AAM.txt')
print(fhand)
```


```python
AAM = "Hello\nIndia"
print(AAM)
```

    Hello
    India
    

## Reading a file


```python
xfile = open('AAM.txt')
for cheese in xfile:
    print(cheese)
```

    India is celebrating 75th year of independence
    
    


```python
# Coounting Lines

fhand = open('AAM.txt')
count = 0 
for line in fhand:
    count = count + 1
print('Line Count:', count)
```

    Line Count: 1
    


```python
fhand = open('AAM.txt')
inp = fhand.read()
print(len(inp))
```

    47
    


```python
print(inp[:20])
```

    India is celebrating
    


```python
fhand = open('AAM.txt')
for line in fhand:
    if line.startswith("India"):
        print(line)
```

    India is celebrating 75th year of independence
    
    


```python
fhand = open('AAM.txt')
for line in fhand:
    if line.startswith("India:"):
        print(line)
```


```python
fhand = open('AAM.txt')
for line in fhand:
    line = line.rstrip()
    if line.startswith("India"):
        print(line)
```

    India is celebrating 75th year of independence
    


```python
#skipping with continue

fhand = open('AAM.txt')
for line in fhand:
    line = line.rstrip()
    if not line.startswith("India"):
        continue
    print(line)

```

    India is celebrating 75th year of independence
    


```python
# using in to select lines

fhand = open('AAM.txt')
for line in fhand:
    line = line.rstrip()
    if not 'independence' in line:
        continue
    print(line)

```

    India is celebrating 75th year of independence
    


```python
#prompt file name

fhand = input('Enter the file name: ')
fhand = open(fhand)
count = 0 
for line in fhand:
    if line.startswith("India"):
        count = count + 1
print('There were', count, 'subject line in', fhand)
```

    Enter the file name: AAM.txt
    There were 1 subject line in <_io.TextIOWrapper name='AAM.txt' mode='r' encoding='cp1252'>
    


```python
# bad file names

fhand = input('Enter the file name: ')
try:
    fhand = open(fhand)
except:
    print('File cannot be opened', fhand)
    quit()

    for line in fhand:
    if line.startswith("India"):
        count = count + 1
print('There were', count, 'subject line in', fhand)

```

    Enter the file name: AAM
    File cannot be opened AAM
    There were 1 subject line in AAM
    

# Chapter 8: Lists


```python
print([1,24,76])
```

    [1, 24, 76]
    


```python
print(['red','yellow','blue'])
```

    ['red', 'yellow', 'blue']
    


```python
print[1,24,76]
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Input In [3], in <cell line: 1>()
    ----> 1 print[1,24,76]
    

    TypeError: 'builtin_function_or_method' object is not subscriptable



```python
print([1, [5, 6], 7])
```

    [1, [5, 6], 7]
    


```python
friends = ['Raj','Yash','Nikhil']
for friend in friends:
    print('Happy Independence Day', friend)

    
```

    Happy Independence Day Raj
    Happy Independence Day Yash
    Happy Independence Day Nikhil
    Done
    


```python
friends = ['Raj','Yash','Nikhil']
print(friends[1])
```

    Yash
    


```python
# Lists are mutable

lotto = [2,14,26,41,63]
print(lotto)
```

    [2, 14, 26, 41, 63]
    


```python
lotto = [2,14,26,41,63]
lotto[2] = 114
print(lotto)
```

    [2, 14, 114, 41, 63]
    


```python
lotto = [2,14,26,41,63]
print(len(lotto))
```

    5
    


```python
# Loops

friends = ['Raj','Yash','Nikhil']

for friend in friends:
    print('Happy Independence Day', friend)

for i in range(len(friends)):
    friend = friends[i]
    print('Happy Independence Day', friend)
```

    Happy Independence Day Raj
    Happy Independence Day Yash
    Happy Independence Day Nikhil
    Happy Independence Day Raj
    Happy Independence Day Yash
    Happy Independence Day Nikhil
    


```python
# Loop operations

a = [1,2,3]
b = [4,5,6]
c= a + b
print(c)
print(a)
```

    [1, 2, 3, 4, 5, 6]
    [1, 2, 3]
    


```python
# Slicing

t = [8,2,4,9,3,1]
t[1:3]
```




    [2, 4]




```python
t = [8,2,4,9,3,1]
t[:4]
```




    [8, 2, 4, 9]




```python
t = [8,2,4,9,3,1]
t[3:]
```




    [9, 3, 1]




```python
t = [8,2,4,9,3,1]
t[:]
```




    [8, 2, 4, 9, 3, 1]




```python
x = list[]
type(x)
```


      Input In [26]
        x = list[]
                 ^
    SyntaxError: invalid syntax
    



```python
x = list()
type(x)
```




    list




```python
dir(x)
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
# building a list from scratch

stuff = list()
stuff.append('book')
stuff.append(99)
print(stuff)
stuff.append('cookie')
print(stuff)
```

    ['book', 99]
    ['book', 99, 'cookie']
    


```python
# checking if something is in List

some = [1,3,5,7,9]
9 in some
```




    True




```python
some = [1,3,5,7,9]
19 in some
```




    False




```python
some = [1,3,5,7,9]
11 not in some
```




    True




```python
# list are in Order

friends = ['Raj','Yash','Nikhil']
friends.sort()
print(friends)
print(friends[1])
```

    ['Nikhil', 'Raj', 'Yash']
    Raj
    


```python
num = [3,41,52,71,64,19]
print(len(num))
print(max(num))
print(min(num))
print(sum(num))
print(sum(num)/len(num))
```

    6
    71
    3
    250
    41.666666666666664
    


```python
# Strings vs Lists

abc = 'with three words'
stuff = abc.split()
print(stuff)
print(len(stuff))
print([0])
```

    ['with', 'three', 'words']
    3
    [0]
    


```python
for w in stuff:
    print(w)
```

    with
    three
    words
    


```python
line = 'A lot'
etc = line.split()
print(etc)
```

    ['A', 'lot']
    


```python
line = 'first;second;third'
thing = line.split()
print(thing)
print(len(thing))
```

    ['first;second;third']
    1
    


```python
line = 'first;second;third'
thing = line.split(';')
print(thing)
print(len(thing))
```

    ['first', 'second', 'third']
    3
    


```python
fhand = open('mbox-short.txt')
for line in fhand:
    line = line.rstrip()
    if not line.startswith('From'):
        continue
    words = line.split()
    print(words[1])
        
```

    ankur.bhattacharjee@outlook.com
    stephen.marquard@uct.ac.za
    stephen.marquard@uct.ac.za
    louis@media.berkeley.edu
    louis@media.berkeley.edu
    zqian@umich.edu
    zqian@umich.edu
    rjlowe@iupui.edu
    rjlowe@iupui.edu
    zqian@umich.edu
    zqian@umich.edu
    rjlowe@iupui.edu
    rjlowe@iupui.edu
    cwen@iupui.edu
    cwen@iupui.edu
    cwen@iupui.edu
    cwen@iupui.edu
    gsilver@umich.edu
    gsilver@umich.edu
    gsilver@umich.edu
    gsilver@umich.edu
    zqian@umich.edu
    zqian@umich.edu
    gsilver@umich.edu
    gsilver@umich.edu
    wagnermr@iupui.edu
    wagnermr@iupui.edu
    zqian@umich.edu
    zqian@umich.edu
    antranig@caret.cam.ac.uk
    antranig@caret.cam.ac.uk
    gopal.ramasammycook@gmail.com
    gopal.ramasammycook@gmail.com
    david.horwitz@uct.ac.za
    david.horwitz@uct.ac.za
    david.horwitz@uct.ac.za
    david.horwitz@uct.ac.za
    david.horwitz@uct.ac.za
    david.horwitz@uct.ac.za
    david.horwitz@uct.ac.za
    david.horwitz@uct.ac.za
    stephen.marquard@uct.ac.za
    stephen.marquard@uct.ac.za
    louis@media.berkeley.edu
    louis@media.berkeley.edu
    louis@media.berkeley.edu
    louis@media.berkeley.edu
    ray@media.berkeley.edu
    ray@media.berkeley.edu
    cwen@iupui.edu
    cwen@iupui.edu
    cwen@iupui.edu
    cwen@iupui.edu
    cwen@iupui.edu
    cwen@iupui.edu
    


```python
words = line.split()
email = words[1]
print(email)
```

    ankur.bhattacharjee@outlook.com
    


```python
# Strings, Files, Lists, Gaurdian Pattern

han = open('mbox-short.txt')

for line in han:
    line = line.rstrip()
    wds = line.split()
    if len(wds) < 3 or wds[0] != 'From':
        continue
    print(wds[2])
```

    Sun
    Sat
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Fri
    Thu
    Thu
    Thu
    Thu
    Thu
    Thu
    

# Chapter 9: Dictionaries


```python
purse = dict()
purse['money'] = 12
purse['candy'] = 3
purse['tissues'] = 75
print(purse)
print(purse['candy'])
```

    {'money': 12, 'candy': 3, 'tissues': 75}
    3
    


```python
purse['candy'] = purse['candy'] + 2 
print(purse['candy'])
```

    5
    


```python
# Counting

ccc = dict()
ccc['csev'] = 1
ccc['cwen'] = 1
print(ccc)
```

    {'csev': 1, 'cwen': 1}
    


```python
ccc['cwen'] = ccc['cwen'] + 1
print(ccc)
```

    {'csev': 1, 'cwen': 2}
    


```python
counts = dict()
names = ['csev', 'cwen', 'zqian', 'cwen']
for name in names:
    if name not in counts:
        counts[name] = 1
    else:
        counts[name] = counts[name]+ 1
print(counts)
```

    {'csev': 1, 'cwen': 2, 'zqian': 1}
    


```python
# counting words in text

# counting pattern
counts = dict()
print('Enter a line of text:')
line = input('')

words = line.split()
print('Words:', words)

print('Counting...')
for word in words:
    counts[word] = counts.get(word,0) + 1
print('Counts', counts)
```

    Enter a line of text:
    who are you
    Words: ['who', 'are', 'you']
    Counting...
    Counts {'who': 1, 'are': 1, 'you': 1}
    


```python
 # two iteration variables

jjj = {'chuck':1, 'Fred': 42, 'jan':200, 'june': 54}
for aaa,bbb in jjj.items():
    print(aaa,bbb)
```

    chuck 1
    Fred 42
    jan 200
    june 54
    


```python
name = input('Enter file: ')
handle = open(name)

counts = dict()
for line in handle:
    words = line.split()
    for word in words:
        counts[word] = counts.get(word,0) + 1

bigcount = None
bigword = None
for word, count in counts.items():
    if bigcount is None or count > bigcount:
        bigcount = word
        bigcount = count

print(bigword, bigcount)
```

    Enter file: mbox-short.txt
    None 353
    


```python
# counting word frequency using a dictionary

fname = input('Enter file: ')
if len(fname) < 1 : 
    fname = 'clown.txt'
hand = open(fname)

for lin in hand:
    lin = lin.rstrip()
    print(lin)
    wds = lin.split()
    for w in wds:
        if w in di:
            di[w] = di[w] + 1
        else:
            di[w] = 1
            print('**NEW**')
        print(w,di[w])
```


```python

```
