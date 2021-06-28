# Overview of Azure core services

## [Compute](002-compute.md) - link to notes

- Azure Virtual Machines
- Azure App Service
- Azure Container Instances and Azure Kubernetes Service
- Azure Functions
## [Networking](002-networking.md) - link to notes

- Azure Virtual Network
- Azure Virtual Gateway
- Azure ExpressRoute

## [Storage](002-storage.md) - link to notes

- Azure Blob Storage
- Azure Disk Storage
- Azure Files Storage
- Azure Blob Access tiers

## [Databases and analytics](002-databases-analytics.md) - link to notes

- Azure Cosmos DB
- Azure SQL Database
- Azure SQL Managed Instance
- Azure Database for MySQL
- Azure Database for PostgreSQL
- Azure Synapse Analytics
- Azure HDInsight
- Azure Databricks
- Azure Data Lake Analytics

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


