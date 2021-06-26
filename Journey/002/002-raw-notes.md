RAW NOTES
## Overview of Azure Services
Microsoft Azure is a collection of services that organizations can use.

Azure has its own datacenters, don't need to have it, maintain infra and scale resources for you.

## Compute
- Azure VMs  
'lift and shift' migration
from on-premise to virtual
IaaS

- Azure App Service - PaaS  
but... if it's not a mobile or web app then cannot use AAS

- Azure Container Instance  
self-contain software env e.g., complete app + all dependencies  
containers are like VMs but they don't include OS
use Azure Container Instance to run container using a single command

but when more complex applications then
- Azure Kubernetes Service  
easy to deploy and manage multi-container apps

- Azure Functions  
something like Azure Apps but you use to do single task and you pay only when it gets used

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
