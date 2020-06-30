# Containers

Take aways: 

How we arrived at containers is not a single path journey.

> Container is a concept to achieve virtualization. To run isolated processes.

***

Computers in 1950s

<img src="./pic1.png" height="200">

Now

<img src="./pic2.jpg" height="200">

Link 1

> Computing power and memory has increased (Exploded)

Story of how computers became small and powerful.

Requirements of computation. Solutions



### Cloud computing

* PaaS 
* IaaS 
* Faas 
* SaaS 

### Why Virtualization?

* Use the resources effectively.
* Resource management.
* Software with different dependencies.
* Run untrusted software.
* Don't disturb other processes.
* Scaling independently and runtime limitations.
* Fault tolerence.

Isolations

* Networking
* Storage
* Computation

## Backstory

Why Linux/Unix - it's open sourced

Chroot in introduced 4.2BSD, which is used to change the root directory of the user.

> Unix philosophy - Evertything is a file 

Linux Root directory

[File Hierarchy Standard](https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard)

> How can we use `chroot`?

<img src="./pic3.png" height=200>

Linux /proc folder

> chroot is not meant to do that. No one knows too.

___

FreeBSD Jail addressing security issues. In Unix root is the super user and can do anything. Why solving it.

* A directory subtree
* A hostname
* An IP address
* process/command to run inside

[Try creating a Jail](https://www.geeksforgeeks.org/linux-virtualization-using-chroot-jail)

___

2001
Solaris zones which isolated files, processes and was similar to containers.

___

2006
Amazon EC2 with resizable computing and pay for what you use. Uses VMs as we know today which virtualizes hardware instead of operatig system.

___

Linux Containers (LXC)


### Quest for virtualization

* BSD Jails
* Solaris Zones
* VMs
* Containers (Linux containers)



## So what is a Linux container?

Google 

Namespaces provide containers with their own view of the underlying Linux system, limiting what the container can see and access.

* Provides its own view of network stacks (Network devices, routing tables, IP addresses, port numbers etc)
* Process IDs, every process is ultimately run on the underlying kernel but the parent process of the container is one of the processes run in the kernel.
* Disk mounts on the system have a different file system respective to containers.
* Interprocess communication is restricted to processes within the container namespaces.
* Individual UID and GID ranges.
* Own hostname and NIS domain name which is individual to each container.


## Docker

Cloud foundry, rocket

Kubernettes..

__March 21 2013__

Links 1

Docker is a 


### VMs and Containers architecture

Both provide cirtulization as we know. Their archetectural differences are as follows.


Microservice architectures and unix philosophy.


#serverless is meaningless unless we run on containers.

### Links

1. [No.of LXCs you can run on your machine](https://ubuntu.com/blog/how-many-containers-can-you-run-on-your-machine)
2. [Unix Philosophy](https://homepage.cs.uri.edu/~thenry/resources/unix_art/ch01s06.html)
2. [Future of Linux containers](https://www.youtube.com/watch?v=wW9CAH9nSLs)

