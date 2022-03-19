# List Comprehensions
***List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list.***

***Notes about Lists Comprehensions***
List comprehension methods are an elegant way to create and manage lists.

In Python, list comprehensions are a more compact way of creating lists. 

More flexible than for loops, list comprehension is usually faster than other methods.

***Syntax***

- _The Syntax_
newlist = [expression for item in iterable if condition == True]

The return value is a new list, leaving the old list unchanged.

- _Condition_

The condition is like a filter that only accepts the items that valuate to True.

- Example : 
```
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits if "a" in x]

print(newlist)    #Output ==> ['apple', 'banana', 'mango']

fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

mylist = [x for x in fruits if "a"  not in x]

print(mylist)   #Output ==> ['cherry', 'kiwi']

```
***Iterable***

- The iterable can be any iterable object, like a list, tuple, set etc.

- Example

You can use the range() function to create an iterable:

```
newlist = [x for x in range(10)]

print(newlist)             Output == >[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

newlist = [x for x in range(10) if x < 5]

print(newlist)              Output == >[0, 1, 2, 3, 4]
```

- Example : Using list comprehensions with strings
```

authors = ["Ernest Hemingway","Langston Hughes","Frank Herbert","Toni Morrison","Emily Dickson","Stephen King"]


letters = [ name[0] for name in authors ]
print(letters)          #Output == >['E', 'L', 'F', 'T', 'E', 'S']
```



***Learning to make use of advanced features like list comprehension will save time and improve productivity***