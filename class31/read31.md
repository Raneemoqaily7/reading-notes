# Django REST Framework & Docker

With Docker we no longer have to mess around with virtual environments. We can faithfully reproduce a production environment locally. Docker is a complex beast under the hood. However a little knowledge can take you a long way, that's the goal of this guide.


## Linux Containers

Virtualization has its roots in the beginning of computer science. A typical guest operating system can easily take up 700MB of size. For most applications, a virtual machine provides far more resources than are needed. Docker is really just Linux containers which are a type of virtualization.

Most computers rely on the same Linux operating system, so what if we virtualized from that level up? Virtual machines provide a lightweight, faster way to duplicate much of the same functionality. For most applications, a virtual machine provides far more resources than are needed.

## Containers vs Virtual Environments

Virtual environments are great but they rely on a global, system-level installation of Python. We can't run a production database or other services within virtual environments. Compared to Docker containers they are far more limited and therefore less useful for us as coders in the real world.


## Install Docker

- To install Docker we need to download the desktop app on our computer and create a free account ,  It should be at least version 19.

```
$ docker --version
Docker version 19.03.5, build 633a0ea
```

- Docker Compose is an additional tool that is automatically included with Mac and Windows downloads of Docker.   `sudo pip install docker-compose`


To confirm Docker installed correctly we can run our first command `docker run hello-world`

```
Hello from Docker!
This message shows that your installation appears to be working correctly.
```



## Images and Containers

A baking analogy we can use here is as follows:

- A Dockerfile is the recipe for a cake
- An image is a snapshot of the recipe at a given time
- A docker-compose.yml says how to make the cake
- And the container is the actual, baked cake
