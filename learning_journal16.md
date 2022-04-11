# What I Learned 


**WRRC** : Web Request Response Cycle 

- **Client and Server**
1.  Client : A client can be a device or a machine.
 A client program runs on the local machine, requesting service from the server. A client program is a finite program means that the service is started by the user and terminates when the service is completed. For instance, web browser.

A client device is a machine that the end-user uses to access the web. Examples of clients are smartphones, desktops, laptops, etc.
 
 2. A server is like a computer program, which is used to provide functionality to other programs. It can be any computerized process called by a client to distribute the work and share the resources.

It receives and responds to requests made over a network. Server receives the request from the client for a web document, and it sends the requested information to the client's computer.

A device can be both a client and a server at the same time, as an individual system has the ability to provide resources and use them from another system in one go. In a single machine, there can be multiple servers.

3. Protocol : a set of rules we have to follow to achieve something 
-- 
## Http protocol
methods or operations of http request 
- GET : when request some article to get the data (retrieve data to the server)
- POST : send data to be stored in database such as (regestration) 
- PUT : Update an existing data in the server 
- DELETE : Delete some data 

**Data format is very imoprte between Client and server** such as (Json format)

**API** : Application Programming Interface ==> a way of communication between frontend (Frontend(written by javascript language)) and backend (Server ) to transfer the data 

- Main Difference between Cloud Server and Traditional Server

| Cloud Server | Traditional Server |
|----------|:-------------:|
|It refers to delivery of different services such as data and programs through internet on different servers|It refers to delivery of different services on local server|
|It takes place on third-party servers that is hosted by third-party hosting companies|It takes place on physical hard drives and website servers|
|It is more cost effective as compared to tradition computing as operation and maintenance of server is shared among several parties that in turn reduce cost of public services|It is less cost effective as compared to cloud computing because one has to buy expensive equipment’s to operate and maintain server|
|It is more user-friendly as compared to traditional computing because user can have access to data anytime anywhere using internet|It is less user-friendly as compared to cloud computing because data cannot be accessed anywhere and if user has to access data in another system, then he need to save it in external storage medium|
|It requires fast, reliable and stable internet connection to access information anywhere at any time|It does not require any internet connection to access data or information|
|It provides more storage space and servers as well as more computing power so that applications and software run must faster and effectively|It provides less storage as compared to cloud computing|
|Cloud service is served by provider’s support team|It requires own team to maintain and monitor system that will need a lot of time and efforts|
--

## Servless Functions
- cloud excution that enable simpler , and most - cost effective way to build cloud-native applications
- Reducing Time , Complexity , effort ,expensivity  when deploying our applications .
- if we are deploing a single function and we want other webapplecation to act with this function so there iss no need to buy a new server and set Ram's and storage for single or couple functions , so servless functions call only when we need it , once the functions excuted and  done , the charge will be based only for these functions that excuted . the charge will be only perusage.

- its nearly zero configureation .





Serverless functions are a single-purpose, programmatic feature of serverless computing — also simply called “serverless” — a cloud computing execution model where the cloud provider provisions computing resources on demand for its customers and manages all architectures, including cloud infrastructure. Yet despite its name, serverless computing still relies on cloud and physical servers to execute code, the difference being that it abstracts away the servers, operating systems and other infrastructure from developers.

The use of serverless functions offers several significant benefits. It frees developers to focus on application development and better-quality application code, as infrastructure concerns, such as redundant code deployments and autoscaling, are handled by the serverless provider. The organization also saves money by only paying for the computing resources it uses instead of overprovisioning physical hardware or renting cloud instances that go unused.


- If the reqquest is correct and there is no problems ==> 2XX (200 ,201 ,..)
- If the request is not correct and ther is a problem from the client side ==> 4XX (404 ,403,..)
- If the req/res is not correct and there is problem from the server side ==> 5XX (500 , ..)













