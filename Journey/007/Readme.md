# Microsoft Azure Security Solutions

## Shared Responsibility
Which tasks are handled by provider, e.g. Microsoft Azure and which by you?

They depend on the service models: IaaS, PaaS, SaaS, on-premise.

On-premise you are responsible for everything.    

**IaaS** - the cloud provider will be responsible for servers and network hardware, hypervisor. The customer will be responsible for OS, networking config, deployed apps, id managment, and data.

**PaaS** - a cloud provider has responsibilies as in the IaaS plus managing and securing network controls. However, the customer is at least partially responsible for securing and managing applications, user identities, and data.

**SaaS** - the customer is still responsible for ensuring that its data is properly classified, customers will share the responsibility for managing users and end-point devices.

## General Azure Security

### Azure Security Center
Helps to assess and visualize resources in Azure and on-premises.
### Azure Key Vault
Stores and manages tokens, passwords, certificates.
Manages certifactes - you can use it to provision, manage, and deploy public and private TLS and SSL certificates.  

Access requires authentication (Azure Active Directory) and authorization.  
Microsoft cannot get your data.

### Azure Monitor Logs
Collects metrics and logs.
- Analyze log data,
- Create a log alert that sends a notification when the results of the qurey match some result,
- visualize 
- supports insights
- access log queries using CLI, powershell, REST API (what is REST API?)
- automated export of log data 

### Azure Sentinel
it is security information event management (SIEM) and security orchestration automated response (SOAR, whatever it means).
It offers intelligent security analytics and threat intelligence for:
- alert detection,
- threat visibility, 
- proactive hunting (hunt for security threats before allert is triggered),
- threat response.

Tou can collect data on all users, devices, applications, infra, on-premise.

It uses AI to get threats.

Orchestration allows to respond quickly??

Firstly, you need to connect to existing data sources.
It integrates with Azure Monitor Workbooks.