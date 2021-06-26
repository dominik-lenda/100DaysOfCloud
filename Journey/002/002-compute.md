## Compute
- Azure Virtual Machines
- Azure App Service
- Azure Container Instances and Azure Kubernetes Service
- Azure Functions

### Azure Virtual Machines (IaaS)
Virtual machines are software emulations of physical computers. VM is like a physical computer - it has vitual processor, memory, storage, networking resources. You can host operating system on it, run software. It is ideal choice when you want have total control over the OS.

**Virtual machine scale set** are an Azure compute resources that helps o deploy and manage a set of identical VMs. 

**Azure Batch** enables large-scale parallel and high-performance computing.

When to use VMs:
- testing and development,
- running applications in the cloud,
- extending capacity of on-premise,
- disaster recovery.
- migration from a physical to the cloud (lift and shift)

### Azure App Service (PaaS)
Allows to quickly build, deploy, and scale web, mobile, and API apps running on any platform. It has many features that guarantee scalability, security, and compliance requirements. Built-in load balancers and traffic managers provide high-availability.

Types of app services:
- Web apps
- API apps
- WebJobs
- Mobile apps

### Azure Container Instances (PaaS) and Azure Kubernetes Service
Those are compute resources that you can use to deploy and manage containers, which are lighweight, virtualized application environments that include complete apps, all dependencies.

Containers are solution to a problem of VM's limitation to a single operating system. You cannot run multiple OSs per VM. If you want to run multiple instances of an application on a single host machine, containers are the way to go.

**VM virtualizes the hardware.**  
**Container virtualizes the operating system.**

You can use Docker, Azure Container Instances and Azure Kubernetes Service (AKS) to manage containers.

- Azure Container Instances is a simple and fast way to run container in Azure.
- Azure Kubernetes Service is for complex applications. It helps to automate, manage tasks and interact with a large number of containers (*orchestration*).

Containers are great solutions for **microservice architecture**.

### Serverless computing - Azure Functions, Azure Logic Apps 

*Serverless* computing is the abstraction of servers infrastructure, and operating systems. Thus infrastructure is not your responsibility. You pay only for the exact resources you use (*micro-billing*). Great for workloads that respond to incoming events.

VM abstracts the hardware, serverless abstracts VM.


- Azure Functions  

Execute code related to certain task without taking  care of infrastructure. Functions that execute code in many modern languages (C#, Python, JavaScript, more). Use when you want run function in response to event such as timer, message, HTTP request.

Functions runs your code when it's triggered and automatically deallocates resources when it's finished. So you are charged for time when you use CPU. However, VM can still incur costs even when it is not stopped (deallocated).

Functions can be stateless or stateful (durable). The difference is in whether the function restarts everytime (stateless, default) or has the history of its previous works (stateful, Durable Functions).

- Azure Logic Apps  

Similar to functions because also enable trigerring based on incoming events. But Logic Apps execute *workflows* that are designed to automate business scenarios. Besides that you use visual designer on the Azure portal (declarative use).
