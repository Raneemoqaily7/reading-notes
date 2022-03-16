# What I Learn Today 

### randiant : return random integer in range [a,b] , including both end points . 
example:    `def randomizer():`
                `return random.randiant(1,6)`

- **Output1 -- > 4**
- **Output1 -- > 6**
- **Output1 -- > 3** 
*  it will give random iunteger each time the program excuted

-  ***To generate 6 random numbers in tuple***

`roll = tuple([randomizer()  for _ in range(6)])`
- **Output1 -- > (1,5,4,2,1,6)**
- **Output2 -- > (2,1,3,2,2,5)**
- Note that :
1. tuple : recieved List 
2. we can instead using (i) with ( _ ) ; if there is no need to use (i) in the For loop .
            
### Counter from Collections
- Counter is a collection where elements are stored as dectionary keys and their counts are  stored as dictionary values 

```from collections import Counter
    
    ctr = Counter(roll)
    print ( ctr)```
    
- ***Output --> Counter({1: 2, 5: 1, 6: 1, 2: 1, 3: 1})***

### most_common()

ctr = [(4, 1), (6, 1), (5, 1), (3, 1), (1, 2)]

- `print(ctr.most_common(2))`            ***Output -->   [(4, 1), (6, 1)]***
- `print((ctr.most_common()[0]))`        ***Output -->[(4, 1)]***
- `print(ctr.most_common(1))`            ***Output -->(4, 1)***
- `print(ctr.most_common(1)[0][1])`      ***Output --> 1***
- `print(ctr.most_common(2)[1])`         ***Output -->1***
- `print((ctr.most_common(2)[0]))`       ***Output -->6***

***if ctr.most_common()[0][1] == 1 --> check if the all values of ctr is 1***

## Two Types of Requirments
* Functional Requirments : The Requirments realted to software and functionalty that are required from the software it self.

* Non Functional Requirments: Secuirety Of The System , Performance Of The System.


    
    
    