# Python-basics-quick-glance
This repo contains very basic syntax on python for revision for a new learner. Content has been taken from Python for beginners course on coursera.

--  Use Dir on any object to check all methods that can be done on it. Ex:
    l=list()
    dir(l)

## Lists
```python
list=[], l=list() # creates a list
list[3] # used to access elements of a list (Note- indexing starts from index 0)
list[1:4], list[2:], list[:8] # different slicings of a list to get a sublist 
    (Note- [a:b] means a to b, not including b)
list.split() # splits a line into different parts about every space i.e. gives a list of words
list.split('@') # splits the list into different parts about the symbol in single quotes
```

## Dictionaries
```python
dict={}, d=dict() # creates a dictionary: collection of key-value pairs 
dict['key'] # used to access elements of a list (Note- no sequence in preserved in the dict elements)
dict.keys(), list(dict) # returns a list of dictionary keys
dict.values() # returns a list of dictionary values
dict.items() # returns a list of tupples (k,v) with key, value pairs

get('key',default) method:
Used to check if a key is in the list or not. 
If present then returns it's value else initialises that key with a default value.
Ex-
for name in names:
  counts[name]=counts.get(name,0) + 1;
```
## Tuples -- Immutable lists Ch-10
These are more efficient than lists bcoz they can be stored more densely as they are immutable.
```python 
tp=( , , , ..)  tp=tuple() #create a tuple
(x,y)=(2,'Ram')
for (k,v) in d.items() # d is dictionary and d.items gives tuples in key value pairs
    print(k,v)
sorted(d.items(), reverse=True)    
```
Comparing 2 tuples is possible

Simple code using above 3 data structures
Q. Find top 10 most common words in a given file.
Code:
```python 
fname="file.txt"
fhand= open(fname)
for line in fhand:
    words=line.split()
    for word in words:
        counts[word]= counts.get(word,0) + 1

lst=list()
for k,v in counts.items()
    newtup= (v,k)
    lst.append(v,k)

lst=sorted( lst, reverse=True )
for v,k in lst[:10]
    print(k,v)
```

## List comprehension
With this we can write last 8 lines of above code in 1 line
In list comprehension, we define a list not by actual elements but by an expression.
For example: ```python a=[(v,k) for (k,v) in d.items()] ```
So we can write last 8 lines of above code as:
```python
print(sorted( [ (v,k) for k,v in counts.items() ], reverse= True ) )
```
## RegEx - Regular Expressions
Very handy for making searches in strings and documents with specific type of pattern like we want to search all words starting with 'H' and ending with 'o' rather than finding whether 'Hello' is present or not. For this, we use wildcard characters.

Python Regular Expression Quick Guide:

\^        Matches the beginning of a line
\$        Matches the end of the line
\.        Matches any character
\\s       Matches whitespace
\\S       Matches any non-whitespace character
\*        Repeats a character zero or more times
\*?       Repeats a character zero or more times 
         (non-greedy)
\+        Repeats a character one or more times
\+?       Repeats a character one or more times 
         (non-greedy)
\[aeiou]  Matches a single character in the listed set
\[^XYZ]   Matches a single character not in the listed set
\[a-z0-9] The set of characters can include a range
\(        Indicates where string extraction is to start
\)        Indicates where string extraction is to end
