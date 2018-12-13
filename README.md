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
list.split() # splits the lists into different parts about every space i.e. gives a list of words
list.split('@') # splits the lists into different parts about the symbol in single quotes
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
## Tuples -- Immutable lists
These are more efficient than lists bcoz they can be stored more densely as they are immutable.
```python 
tp=( , , , ..)  tp=tuple() #create a tuple
(x,y)=(2,'Ram')
for (k,v) in d.items() # d is dictionary and d.items gives tuples in key value pairs
    print(k,v)
    
```
