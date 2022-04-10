# What is Serverless Computing?

Serverless is a cloud computing model that automatically provisions computing resources required to run applications. Serverless offloads all management responsibility for backend cloud infrastructure and operations tasks to the cloud provider. Customers never pay for idle capacity - they pay only for the resources needed to run their applications.

The term 'serverless' describes the customer's experience with those servers. They are invisible to the customer, who doesn't see them, manage them, or interact with them. Amazon Web Services introduced serverless in 2014 with AWS Lambda. Today every leading cloud service provider offers a serverless platform.

# Serverless pros and cons 

## pros

Serverless allows developers to focus on writing code, not managing infrastructure. Developers can code in any language or framework - Java, Python, node.js - with which they're comfortable. Customers pay for execution only - the meter starts when the request is made, and ends when execution finishes.

Serverless development platforms provide near-total visibility into system and user times, and can aggregate that information systematically. Serverless is a polyglot environment, enabling developers to code in any language or framework - Java, Python, node.js - with which they're comfortable.

## cons 

There are certain applications for which serverless is not favorable, or which present technical and business trade-offs. Because serverless architectures forgo long-running processes in favor of scaling up and down to zero, they also sometimes need to start up from zero to serve a new request.

Serverless architectures are designed to take advantage of an ecosystem of managed cloud services. Vendors may find it difficult or impossible to monitor or debug serverless functions using existing tools or processes.

# venv — Creation of virtual environments

The venv module provides support for creating lightweight "virtual environments" with their own site directories, isolated from system site directories. Each virtual environment has its own Python binary (which matches the version of the binary that was used to create this environment) and can have its own independent set of installed Python packages. The use of venv is now recommended for creating virtual environments for Python 3.3 and 3.4, and is deprecated in 3.6.

Creation of virtual environments is done by executing the command venv:

`python3 -m venv /path/to/new/virtual/environment`

When a virtual environment is active, the VIRTUAL_ENV environment variable is set to the path of the virtual environment. This can be used to check if one is running inside a virtual Environment. You don't need to activate an environment; activation just prepends the virtual Environment's binary directory to your path. The exact mechanism is platform-specific and is an internal implementation detail (typically a script or shell function will be used).

A virtual environment is a directory tree which contains Python executable files and other files which indicate that it is a virtual environment. Common installation tools such as setuptools and pip work as expected with virtual environments. The attributessys.exec_ prefix and.sys.base_ prefix point to the non-virtual environment Python. installation which was used to create the virtual environment (i.e., the Python interpreter is not running).

Users can make a virtual environment active by running an activate script in the virtual environment's executables directory. "Shebang" line processing is supported if you have the Python Launcher for Windows installed. This was added to Python in 3.3 - see PEP 397 for more details. Double-clicking an installed script in a Windows Explorer window should run the correct interpreter.

# http.server — Base Classes for Implementing Web Servers

**HTTP GET**
HTTP GET request is used to request data from a specified resource. Using Python Requests library, you can make a HTTP GET request.

In this tutorial, we shall learn how to send a HTTP GET request for a URL. Also, we shall learn about the response and its components.

In this example, we shall use requests library and send a GET request with a URL.

```
import requests

response = requests.get('https://pythonexamples.org/python-basic-examples/')
```
**HTTP POST**
HTTP POST request is used to create or update a resource in a specified server.

In Python Requests library, requests.post() method is used to send a POST request to a server over HTTP. You can also send additional data in the POST request using data parameter.

In this example, we shall send a POST request to the server with given URL.

```
import requests

response = requests.post('https://pythonexamples.org/', data = {'key':'value'})
```

**Threading and Forking**

A thread is a separate flow of execution. This means that your program will have two things happening at once. But for most Python 3 implementations the different threads do not actually execute at the same time. This is due to interactions with the GIL that essentially limit one Python thread to run at a time.

There is some examples of how to build threaded programs and the problems they solve. If you'd like to explore other options for concurrency in Python, check out Speed Up Your Python Program With Concurrency. Or if you're interested in doing a deep dive on the asyncio module, go read AsyncIO in Python: A Complete Walkthrough.