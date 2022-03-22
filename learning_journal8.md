***What I Learned Today***

- One of the most powerful features of Python is that everything is an object, including functions.  Functions are First Class Object such as (float , int ,str  etc );that  means functions in Python:
1. have types
2. can be sent as arguments to another function
3. can be used in expression
4. can become part of various data structures like dictionaries

***Example ***

- Function to return square of a number
```
L =[3,4,5,6,7]
def sqr(num):
  return num**2

print (apply(L,sqr))
```

- map()	is a Built-in function Returns the specified iterator with the specified function applied to each item

***Example*** : 
```
def myfunc(a):
  return len(a)

x = map(myfunc, ('apple', 'banana', 'cherry'))

#convert the map into a list, for readability:

print(list(x))                       #Output == >[5, 6, 6]

```
## Inner Functions
A function defined inside another function is known as an inner function or a nested function.

You can create functions inside a function and call the insted functions inside the outer function then call the outer function outside .

```
 def outer_func():
      def inner_func():
          print("Hello, World!")
      inner_func()
 

 outer_func()                   #Output == >Hello, World!

```
In this code, you define inner_func() inside outer_func() to print the Hello, World! message to the screen. To do that, you call inner_func() on the last line of outer_func().
                     
```
 def factorial(number):
      # Validate input
      if not isinstance(number, int):
          raise TypeError("Sorry. 'number' must be an integer.")
      if number < 0:
          raise ValueError("Sorry. 'number' must be zero or positive.")
      # Calculate the factorial of number
      def inner_factorial(number):
          if number <= 1:
              return 1
          return number * inner_factorial(number - 1)
      return inner_factorial(number)
 
 factorial(4)         #Output == >24

```
