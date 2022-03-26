# What is a Stack
A stack is a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.

### Common terminology for a stack is
- Push: Adds an item in the stack. Once the stack is full, it is said to be in an Overflow condition.
- Pop: Removes an item from the stack. It follows a reversed order to pop items similar to the way when items are pushed. It is said to be an Underflow condition.
- Peek: View the topmost item in the stack.
- Duplicate: Copy the top item’s value into a variable and push it back into the stack.
- Swap: Swap the two topmost items in the stack.
- Rotate: Move the topmost elements in the stack as specified by a number or move in a rotating fashion


Two concepts for Stack:

**FILO**
***First In Last Out***

This means that the first item added in the stack will be the last item popped out of the stack.

**LIFO**
***Last In First Out***

This means that the last item added to the stack will be the first item popped out of the stack.

***- Steps for Push Operation in Python***
Checks if the stack is full.
If the stack is full, produces an error and exit.
If the stack is not full, increments top to point next empty space.
Adds data element to the stack location, where the top is pointing.
Returns success.

***- Steps for Pop Operation in Python***
Checks if the stack is empty.
If the stack is empty, produces an error and exit.
If the stack is not empty, accesses the data element at which the top is pointing.
Decreases the value of top by 1.
Returns success.

***The functions associated with stack are:***
empty() – Returns whether the stack is empty – Time Complexity: O(1)
size() – Returns the size of the stack – Time Complexity: O(1)
top() – Returns a reference to the topmost element of the stack – Time Complexity: O(1)
push(g) – Adds the element ‘g’ at the top of the stack – Time Complexity: O(1)
pop() – Deletes the topmost element of the stack – Time Complexity: O(1)

***Applications of Python Stack***
Stacks are considered as the backbone of Data Structures. Most of the algorithms and applications are implemented using stacks.

Some of the key applications of Python Stacks are—

used in “undo” mechanism in the text editor.
Language processing:
space for parameters and local variables is created internally using a stack.
compiler’s syntax check for matching braces is implemented by using stack.
support for recursion.
Expression evaluation like postfix or prefix in compilers.
Backtracking (game playing, finding paths, exhaustive searching.
Python Stack is also used in Memory management, run-time environment for nested language features. etc
Used in Algorithms like Tower of Hanoi, tree traversals, histogram problem and also in graph algorithms like Topological Sorting.

***Conclusion***

Python Stack is simple data structures that allow us to store and retrieve data in a sequential fashion. They are very useful in real-world cases. Having a clear understanding of stacks would help us in solving data storage problems in an efficient manner.

The Python stack is an important data structure for realizing solutions to various programming problems. As such, it is even more essential to understand the running time evaluations and working mechanism of these data structures.

# Queue in Python
Like stack, queue is a linear data structure that stores items in First In First Out (FIFO) manner. With a queue the least recently added item is removed first. A good example of queue is any queue of consumers for a resource where the consumer that came first is served first.

***Operations associated with queue are:*** 
 

Enqueue: Adds an item to the queue. If the queue is full, then it is said to be an Overflow condition – Time Complexity : O(1)
Dequeue: Removes an item from the queue. The items are popped in the same order in which they are pushed. If the queue is empty, then it is said to be an Underflow condition – Time Complexity : O(1)
Front: Get the front item from queue – Time Complexity : O(1)
Rear: Get the last item from queue – Time Complexity : O(1)
 

***Implementation***
There are various ways to implement a queue in Python. This article covers the implementation of queue using data structures and modules from Python library.
Queue in Python can be implemented by the following ways:
 

1. list
2. collections.deque
3. queue.Queue


***Implementation using queue.Queue***
Queue is built-in module of Python which is used to implement a queue. queue.Queue(maxsize) initializes a variable to a maximum size of maxsize. A maxsize of zero ‘0’ means a infinite queue. This Queue follows FIFO rule. 
There are various functions available in this module: 
 

maxsize – Number of items allowed in the queue.
empty() – Return True if the queue is empty, False otherwise.
full() – Return True if there are maxsize items in the queue. If the queue was initialized with maxsize=0 (the default), then full() never returns True.
get() – Remove and return an item from the queue. If queue is empty, wait until an item is available.
get_nowait() – Return an item if one is immediately available, else raise QueueEmpty.
put(item) – Put an item into the queue. If the queue is full, wait until a free slot is available before adding the item.
put_nowait(item) – Put an item into the queue without blocking. If no free slot is immediately available, raise QueueFull.
qsize() – Return the number of items in the queue.
 
