# Networking

## Azure Virtual Network

Azure virtual networks (VNets) communicate Azure resources, users on the internet, and on-premises.

VNets have a few key capabilities:
- Isolation and segmentation  
VNet allows you to create many isolated virtual networks. You can create subnets.
- Internet communications
- Communication between Azure resources  
VNets can connect not only VMs but also Azure PaaS solutions such as Power Apps, Azure Kubernetes Service. **Service endpoints** can be used to connect other Azure resources such as Azure SQL databases and storage accounts.
- Communication  with on-premise resources  
**Point-to-site virtual private networks** - Virtual Private Network (VPN) connection between VNet and a computer.  
**Site-to-site virtual private networks** - VPN connection between on-premise VPN device or gateway to the Azure VPN gateway in a virtual network.  
**Azure ExpressRoute** - when you need more bandwidth and security, allows you to apply private connection between that does not travel over the internet.
- Route network traffic  
Route tables  
Border Gateway Protocol Border Gateway Protocol (BGP)  
- Filter network traffic  
Network security groups - allow or block traffic.  
Network virtual appliances
- Connect virtual networks  
VNet peering - connection between VNets.

## Azure VPN Gateway

Virtual Private Networks (VPNs) make secure, encrypted connection between private networks over an untrusted network, typically the public internet.

Exemple is to share sensitive information between different locations.

### VPN gateways

VPN gateway is a type of networking device that connects two or more devices or networks in a VPN infrastructure. It can be a router, server, firewall or sth else.

Azure VPN Gateway instances are deployed to enable the connectivity below:
- Connect on-premises to virtual networks (*site-to-site*)
- Connect individual device to virtual networks (*point-to-site*)
- Connect virtual networks to other virtual networks (*network-to-network*)

Virtual network can have only one VPN, but VPN can point to many others VNets or on-premises.

(*) You need to specify VPN type when deploying it:
- policy-based
- route-based

### VPN gateway sizes

SKU is a size of VPN gateway.

- Basic (only for Dev/Test)
- VpnGw1/Az
- VpnGw2/Az
- VpnGw3/Az

### Deploy VPN gateway

You need six Azure and two on-premise resources before deployment of VPN gateway.

Azure resources required:
- Virtual network 
- GatewaySubnet
- Public IP address
- Local network gateway
- Virtual network gateway
- Conection

On-premise resources required:
- A VPN device
- A IPv4 address

You can increase tolerance for errors by:
- deploying VPN gateways as two instances in an **active/standby**
- deploying VPN gateways as two instances in an **active/active**; when you assign a unique public IP address to each instance
- *related to high-availability of ExpressRoute* - you can provision VPN gateway, which uses the internet, as an alternative method of connectivity
- zone-redundant gateways - VPN gateways and ExpressRout
e gateways can be deployed in zone-reduandant configoration in availability zones

## Azure ExpressRoute

ExpressRoute allows you to extend on-premises networks into the Azure VNets over a *private connection*. ExpressRoute connections don't go over the public internet. It's more expensive option than VPNs. It provides a few benefits in connectivity:
- higher security
- faster speeds
- more reliability
- consistent latencies

Technically speaking, features and benefits are the following:
- Layer 3 connectivity  
**Layer** 3 connectivity can be from a point-to-point or any-to-any network.
- Built-in redundancy  
**Each** connectivity provider uses redundant devices. It guarantees high-availability that is default.
- Connectivity to Microsoft cloud services  
**It** enables access to the Microsoft cloud services: Microsoft Office 365, Azure compute and cloud services, e.g. Azure Virtual Machines, Azure Cosmos DB.
- ExpressRoute Global Reach   
**You** can connect datacentres that are in distanced locations.
- Dynamic routing  
**ExpressRoute** uses the *Border Gateway Protocol* (BGP) routing protocol.

### ExpressRoute connectivity models

- CloudExchange colocation
- Point-to-point Ethernet connection
- Any-to-any connection

