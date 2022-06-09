## Big O Notation and Algorithm Analysis with Python 

Big-O notation is a metrics used to find algorithm complexity. Basically, Big-O signifies the relationship between the input to the algorithm and the steps required to execute the algorithm. It is denoted by a big "O" followed by opening and closing parenthesis.

- The following are some of the most common Big-O functions:


| Name    | Big O|
|----------|:-------------:|
|Constant|	O(c)|
|Linear|	O(n)|
|Quadratic|	O(n^2)|
|Cubic|	O(n^3)|
|Exponential|O(2^n)|
|Logarithmic|O(log(n))
|Log Linear|O(nlog(n))

---

- Now  let's take a look at some examples of constant, linear, and quadratic complexity.

### Constant Complexity (O(C))

- Example 
```
def constant_algo(items):
    result = items[0] * items[0]
    print()

constant_algo([4, 5, 6, 8])
```
- Analysis 

If you draw a line plot with the varying size of the items input on the x-axis and the number of steps on the y-axis, you will get a straight line. To visualize this, execute the following script:

```
import matplotlib.pyplot as plt
import numpy as np

x = [2, 4, 6, 8, 10, 12]

y = [2, 2, 2, 2, 2, 2]

plt.plot(x, y, 'b')
plt.xlabel('Inputs')
plt.ylabel('Steps')
plt.title('Constant Complexity')
plt.show()
```

Output :

![bigO](./big-o-notation-and-algorithm-analysis-python-examples-1.png)

***In the above script, irrespective of the input size, or the number of items in the input list items, the algorithm performs only 2 steps: Finding the square of the first element and printing the result on the screen. Hence, the complexity remains constant..***


### Linear Complexity (O(n))

```
def linear_algo(items):
    for item in items:
        print(item)

linear_algo([4, 5, 6, 8])
```
- The plot for linear complexity with inputs on x-axis and # of steps on the x-axis is as follows:

```
import matplotlib.pyplot as plt
import numpy as np

x = [2, 4, 6, 8, 10, 12]

y = [2, 4, 6, 8, 10, 12]

plt.plot(x, y, 'b')
plt.xlabel('Inputs')
plt.ylabel('Steps')
plt.title('Linear Complexity')
plt.show()
```

For a linear_algo function, the complexity of the for-loop will be equal to the size of the input items array. For instance, if there are 4 items in the items list, and each item is executed 4 times, and so on. In the above example, this means that the number of iterations of the for-loop is linear.

### Finding the Complexity of Complex Functions

```
def complex_algo(items):

    for i in range(5):
        print("Python is awesome")

    for item in items:
        print(item)

    for item in items:
        print(item)

    print("Big O")
    print("Big O")
    print("Big O")

complex_algo([4, 5, 6, 8])
```

-  first, a string is printed 5 times on the console using the print statement
-  Next, we print the input list twice on the screen and finally, another string is being printed three times on the console. 

To find the complexity of such an algorithm, we need to break down the algorithm code into parts and try to find the complexity of the individual pieces.

- Now Let's break our script down into individual parts. In the first part we have:

```
 for i in range(5):
        print("Python is awesome")
```

- The complexity of this part is O(5). Since five constant steps are being performed in this piece of code irrespective of the input.

Next, we have:

```

for item in items:
    print(item)
```

- We know the complexity of above piece of code is O(n).

Similarly, the complexity of the following piece of code is also O(n)

```
for item in items:
    print(item)
```

Finally, in the following piece of code, a string is being printed three times, hence the complexity is O(3)

```
print("Big O")
print("Big O")
print("Big O")
```

To find the overall complexity, we simply have to add these individual complexities. Let's do so:

O(5) + O(n) + O(n) + O(3)

Simplifying above we get:

O(8) + O(2n)

- We said earlier that when the input (which has length n in this case) becomes extremely large, the constants become insignificant i.e. twice or half of the infinity still remains infinity. Therefore, we can ignore the constants. The final complexity of the algorithm will be O(n).


## Conclusion
The Big-O notation is the standard metric used to measure the complexity of an algorithm. In this article, we studied what Big-O notation is and how it can be used to measure the complexity of a variety of algorithms. We also studied different types of Big-O functions with the help of different Python examples. Finally, we briefly reviewed the worst and best case complexity along with the space complexity.