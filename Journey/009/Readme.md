## Database Security 

### Azure SQL Firewall Rules
Connections from the Internet to the specific SQL database or the whole SQL server (all databases) will have to pass firewall. The firewall examines IP ranges. You can define 128 server-level and database-level firewall rules.
### Azure SQL Always Encrypted
Protects sensitive data that are stored in an Azure SQL Database or SQL Server database, e.g. credict card numbers. Clients can encrypt sensitive data themselves. Unauthorized user cannot access sensitive data, even admins.

### Azure SQL Transparent Data Encryption (TDE)
TDE is used to protect Azure SQL Databases, Azure SQL Managed Instances, and Azure Synapse from malicious offline activites.  
It performs real-time encryption and decryption if data related to backups, log files.

### Azure SQL Database Auditing
Works along with Azure SQL Database and Azure Synapse Analytics will track database events so you can store them. Helps to maintain regulatory compliance.  
Helps to monitor suspicious event, anomalies.
Avoid server and database autditing. Best way is to enable server-level blib auditing only and leave database-level auditing disabled for all databases.

## Dynamic Data Masking
Take care of sensitive data by masking it for users who shouldn't see it.

In a simple form: 
XXXX-XXXX-XXXX-9999

While configuring data masking policy you need to specify SQL masking rules, masking functions and decide which users should be excluded from masking.

A feature for Azure SQL Managed Instance, and Azure Synapse Analytics.

## Identity and Access Management

### Role-based access control (or RBAC)
You can manage which users have access to what Azure resources, what those users can do with those resourcces. RBAC is an authorization system built on Azure Resource Manager.

### Azure Active Directory
Cloud-based identity and access management. Used to allow users to sign in and access resources.

Very general, you can control access to internal resource and external applications.
### Azure Active Directory B2B
Allows organization to securely share their apps and services with guest uests from external organizations.

### Azure Active Directory B2C
Allows organizations' customers to access apps via single sign-on.
Support OpenID, OAuth 2.0, SAML. 

### Azure Active Directory Domain Services
Domain controller as a service.

I do not understand this :)
### Azure Multi-Factor Authentication
Layerd approach to authentication. 
- sth you know (password)
- sth you posses (smartphone)
- sth you are (fingerprint)

 ## Networking Security

 ### Network Security Group
 Allow or deny inbound/outbound network traffic.

 You can create as many custom rules as you need to control traffic and secure your resources, while you cannot delete default rules. 

 ### Azure VPN Gateway
 Secure connection between Azure VNet and on-prem.

 ### Azure ExpressRoute
Secure and robust way to connect on-prem and Azure. It uses private connection, not the internet.

### Web Application Firewall (WAF)
Protect web apps. Included in Application Gateway service amnd with the Front Door service. High-availability and unrestricted cloud scalability.

 ### Azure Firewall
Helps to protect Azure Network resources. 

 ### Azure DDoS Protection
- Automatically enabled
- Always-on traffic monitoring 
- Real-time mitigation
- Uses ML algo

Using it you apply protection policies to the public IP addresses that are associated with resources deployed in VNets including Application Gateway, Load Balancer, Service Fabric Instances.

 ### Virtual Network Service Endpoints
Service endpoints are used to extend the private address space of an Azure VNet (why is it needed?)
 
 Not sure if I get it.