# Overview of Azure core services

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

## Networking
- Azure Virtual Network (VNet)  
similar to on-premise;
each VM in VNet gets IP address and can be communicated with other VMs
Communication between VMs; VMs - the 

- Subnets  
You can divide VNets into subnets and route them;
in-bound traffic

- VNet peering
communications between VNets; or to be more exact; communication between VMs in one VNet and VMs in another VNet; other resources such as Kubernetes clusters can be in VNets too; VM is just a simple example of a resource

- Azure VPN
Secure connection between VNet and on-premise networks a) Virtual Private Network is on-premise -- encrypted traffing in the public Web -- VNet b) ExpressRoute on-premise --dedicated, fast and reliable connection -- VNet; but of course ExpressRoute is expensive 


## Storage
- Azure Blob Storage  
object storage; collection of files; no hierarchical folder structure; it's flat, for videos, images, etc.
HOT (frequent), COOL (infrequent), ARCHIVE (backup, lowest cost)  
if you need hierarchical file storage

- Azure File Storage  
hierarchical structure; files for Windows servers

- Azure Data Lake Storage Gen2  
Hadoop-compatibile for data analytics apps

- Azure SQL databases  
relational databases, very similar to sql server; open source version are also available:

- Azure DB Open Source   
Azure Database for MySQL, Azure Database for Maria DB, Azure Database for PostgreSQL online transactions processing; on

I really like the transistions between learned concepts

- Azure Synapse Analytics  
data warehouse; integration of many services

- Azure Cosmos DB
SQL Database not enough; the traffic to high so use Azure Cosmos DB; NoSQL, not relational; sacraficing some power to meet demand of users

Cosmos DB can scale globally

- Azure Cache for Redis  
can speed application's data by 
caching frequently requested data
cashing caching - almost funny
caching is important; is like storing data/files closer to the users

## Using the Azure Portal
There are many ways to interact with Azure
- Azure Portal (Web, mobile app)
- Azure CLI
- Azure PowerShell
- SDK (Java, JavaScript, Python, etc.)

SDK is needed if you do some programming in some programming langugae and want to interact with Azure


### Use Azure Portal to create a resource -> VM
Microsoft creates Billing Account and Subscription, both involved in billing

BASICS
- **Billing Account**    
is an your agreement or orgniazation's agreement to use 
- **Subscription**  
a collection of all of resources you use 

you may want multiple subscriptions in one billing account; 
each subscription generates a seperate invoice; it is good to have separate subscriptions for security or other reasons

- **Resource Group**  
a collection of resources, like subscription; but subscription can have multiple resource group.

- **Location**  
regions, availability zones;
region that supports availability zones has at least three data centers. It is good to put VMs in different zones. If one is loaded, has troubles other still work.

- Image
Ubuntu Server example

- Size

- Administrator account
best to use ssh

- inbound port rules
access from the internet

DISKS  
hdd/ssd/premium etc

NETWORK
default -> vnet, subnet, and public IP address

**mini-tutorial on web app??**

## Service Categories
Other important services than those related to compute, storage, networking, database

### Migration
Azure Migrate helps organizations migrate to the cloud.  
What does Azure Migrate do?
I Discovers on-premise; physical, virtual
II Assesses the machines;
III It assesses if it's good a condition to migrate; shows costs
integrated with other tools
It is easy to integrate Active Directory with Azure Active Directory,
so migration of identities is possible.

### DevOps
the idea is that you can **automate** many stages of application building:
dev stage/testing/production.

The most important
- **Azure Pipelines** allows to create automated workflows to build, test, and deploy

- Azure DevTest Labs helps to organize non-production env; so developing is testing is autometed, quicker, better;

- Azure Content Delivery Network (it is in DevOps category?? why?)
caches frequently accessed content and brings it to serveres closer to a web user

### Internet of Things (IoT)
many devices connected to the cloud

- Azure IoT Central (SaaS)  
creating IoT app without any code

- Azure IoT Hub  
you have more control; IoT Central uses it 

- Azure Sphere   
gives layers of protection

### 


