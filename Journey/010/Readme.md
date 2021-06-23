# Pricing and Support

Pricing is based on time, bandwidth, or storage consumption.

The goal for this course is to understand how services are priced and metered.

## Azure Subscription
It is a single billing unit for Azure resources that is linked to single account.

Three types of subscriptions:
- Free
- Pay-as-you-go
- member offers (offer reduced rates; MSDN Platform, Visual Studio subscribers)

You can have more than one subscription.

## Planning and managment
Three purchasing options:
- Enterprise
Agreement between the enterprise and Microsoft. The agreement to purchase a negotiated amount of Azure services.

15%-45% savings

- Web Direct
When customers sign up using the Azure website. Pay-as-you go, billed monthly.

- Cloud Solution Provider
Agreement between Microsoft and Microsoft partner companies. Billing for Azure usage 

### Planning and management of Azure Costs

Charges mostly are based on usage, which is called **metering**. Some resources are execptions, e.g. virtual networks.

Metering is based on a few factors, but most importantly is based on the type of resource:
- networks - bandwidth
- running time for IAAS virtual machines
- storage accounts - storage capacity
- virtual machine - size and time

Usage costs may vary between regions.

**Networks**  
Chargers mostly for egress traffic (dat out) after the first 5GB/Month ($0.087 per GB) and is based on the zone (currently Azure has 4 zones).

For a planning use Pricing Calculator.

You can use many benefitc such as Azure Hybrid benefit by using your existing Windows licence.

Another tool is the Total Cost of Ownership Calculator. Helps to estimate cost savings that result from migration.

### Best Practices
- Azure Price Calculator for cost estimation per resource.

- Spending Limits
When the limit is reached, a subscription is suspended until the beginning of the next billing cycle.

- Tags
A way to group resoueces to track costs.

- Azure Reservations
Paying in advance for products.
Pay for a VM for 1 year befor or 3 year before. It is possible to save up to 72% over the pay-as-you-go costs.

- Azure Advisor
Tool built-in Azure portal with four blades:  
a) High Availability  
b) Security  
c) Performance  
d) **Cost**  

Cost blaed is a redirection to Cost Management platform.

- Azure Cost Management
a great tool to monitor costs per resource.

### Support Options

- Developer
For trial and non-production environemtne. Response within 8 hours, in normal business hours.
- Standard
For production workloads. 24/7, response in 1 hour.
- Professional Direct
24/7, response within 1 hour, additional benefits such as training.

- Premier
24/7, response in 15 minutes.

### Azure Service Level Agreements
SLA is a formal document that provides specific terms that state the level of service that will be provided to a customer.

### Service Lifecycle

- Preview Features
you can beta test prerelease versions of products and features. Private, public preview.

- General Availability (GA)
Successfully tested products are released to customers as a part of GA