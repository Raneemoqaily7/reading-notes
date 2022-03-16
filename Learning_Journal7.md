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

   `from collections import Counter`
    
    `ctr = Counter(roll)
    print ( ctr)`
    
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


# 
**Some Notes Before Starting**
* Client determine the process of the App and give the senarios.
* In the file name (file.sim.txt) 
- sim (simulation): doesnt effect in the code , it just a refference for other developers to know that is the file used for simulation .
- Flo file take the responsipilty to get the user input from the simulation files and extract them to test it for us  .
- Train your mind not to overthinking just follow the requeirment of the senario

* The Process 
1. write your functions in  file.py
2. import the module from  flo.py

`from tests.flow.flo import Flo

def test():
    Flo.test("path of the simulater_file_path")`

3. Flo will take the responpility to test .

# Dependency Injection
 Dependency Injection is a technique in which an object receives other objects that it depends on.

  * Benefits:
  1. Methods are easier to test
  2. Dependencies are easier to mock
  3. Tests doesn't have to change every time that we extend our application
  4. It's easier to extend the application
  5. It's easier to maintain the application

# What does the Dependency Injector do?
With the dependency injection pattern objects loose the responsibility of assembling the dependencies. The Dependency Injector absorbs that responsibility.

Dependency Injector helps to assemble and inject the dependencies.

It provides a container and providers that help you with the objects assembly. When you need an object you place a Provide marker as a default value of a function argument. When you call this function framework assembles and injects the dependency.

from dependency_injector import containers, providers
from dependency_injector.wiring import Provide, inject


class Container(containers.DeclarativeContainer):

    config = providers.Configuration()

    api_client = providers.Singleton(
        ApiClient,
        api_key=config.api_key,
        timeout=config.timeout,
    )

    service = providers.Factory(
        Service,
        api_client=api_client,
    )


@inject
def main(service: Service = Provide[Container.service]):
    ...


if __name__ == "__main__":
    container = Container()
    container.config.api_key.from_env("API_KEY", required=True)
    container.config.timeout.from_env("TIMEOUT", as_=int, default=5)
    container.wire(modules=[__name__])

    main()  # <-- dependency is injected automatically

    with container.api_client.override(mock.Mock()):
        main()  # <-- overridden dependency is injected automatically

    
    
    
   -  Resources 
    * testdriven.io  