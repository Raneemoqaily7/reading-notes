# Dunder (Magic, Special) Methods

***What Are Dunder Methods?***

Python's special methods are a set of predefined methods you can use to enrich your classes. These "dunders" or "special methods" in Python are also sometimes called "magic methods". But using this terminology can make them seem more complicated than they really are.

```
class Member:
    def __init__(self ,firstName,lastName,gender):    #This is a constructor wrote  the data you want use in (init)
        self.fName=firstName
        self.lName=lastName
        self.gender=gender
```


Python has a set of built-in methods and __call__ is one of them. The __call__ method enables Python programmers to write classes where the instances behave like functions and can be called like a function. When the instance is called as a function; if this method is defined, x(arg1, arg2, ...) is a shorthand for x.__call__(arg1, arg2, ...).

object() is shorthand for object.__call__()

Example 1:


class Example:
    def __init__(self):
        print("Instance Created")
      
    # Defining __call__ method
    def __call__(self):
        print("Instance is called via special method")
  
 Instance created
e = Example()
  
 __call__ method will be called
e()
Output :

Instance Created
Instance is called via special method


##  What is probability?
Probability seeks to answer the question, "What is the chance of an event happening?". The quintessential representation of probability is the humble coin toss. An ideal coin will have a 1-in-2 chance of being heads or tails. We can use statistics to calculate probabilities based on observations from the real world.


## Random Variable
A random variable is a variable whose possible values are numerical outcomes of a random phenomenon. There are two types of random variables, discrete and continuous.

A discrete random variable is one which may take on only a countable number of distinct values and thus can be quantified. For example, you can define a random variable X to be the number which comes up when you roll a fair dice. X can take values : [1,2,3,4,5,6] and therefore is a discrete random variable.