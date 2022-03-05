# Classes and Objects
Python is an object oriented programming language.
Almost everything in Python is an object, with its properties and methods.
A Class is like an object constructor, or a "blueprint" for creating objects.

- What is the classes and the objects ? 
Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.
- - 
*  Creat Class with variables
To Create a class named MyClass, with a property named value use class keyword :

class MyClass :
   variable = value
   x = 10

* Create object 
Now we can  use the class named MyClass to create object 

object1 = MyClass()

- Accessing Object Variables 
print (object1.variable) ==> output = value 
print ( object1.x )      ==> output = 10

- Changing the values 
You can create multiple different objects that are of the same class(have the same variables and functions defined)
if we were to define another object with the "MyClass" class and then change the string in the variable above
object2 = MyClass()
object2.x = 20

print (object2.x ) ==> output = 20
print (object1.x)  ==> output = 10 

* Creat Class with functions
    class MyClass:
      def func(self) :
        print ("Hello, World!)

- Accessing Object functions
 object1 = MyClass()
 object1.func()     ==> output = Hello, World!

 - - 
- The examples above are classes and objects in their simplest form, and are not really useful in real life applications.
To understand the meaning of classes we have to understand the built-in __init__() function.

* The __init__() Function
All classes have a function called __init__(), which is always executed when the class is being initiated.

class car :
   def __init__(self , brand ,color):
      self.brand = brand
      self.color = color
p = car("BMW" , "Black")

print (p.brand) ==> output = BMW
print (p.color) ==> output =Black

Note: The __init__() function is called automatically every time the class is being used to create a new object.

# To Practice Try This Excercise at 
[Classes and Objects exercise](https://www.learnpython.org/en/Classes_and_Objects#google_vignette)

![show solution](./images/exe_obj_and_class.png)


 





