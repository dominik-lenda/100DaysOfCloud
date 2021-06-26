## Networking

### Azure Virtual Network fundamentals

Azure virtual networks (VNets) communicate Azure resources, users on the internet, and on-premises.

VNets have a few key capabilities:
- Isolation and segmentation  
VNet allows you to create many isolated virtual networks. You can create subnets.
- Internet communications
- Communication betwee Azure resources
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

### Azure VPN Gateway fundamentals
Virtual Private Networks (VPNs) make secure, encrypted connection between private networks over an untrusted network, typically the public internet.

Exemple is to share sensitive information between different locations.

**VPN gateways**  
Azure VPN Gateway instances are deployed to enable the connectivity below:
- Connect on-premises to virtual networks (*site-to-site*)
- Connect individual device to virtual networks (*point-to-site*)
- Connect virtual networks to other virtual networks (*network-to-network*)

Virtual network can have only one VPN, but VPN can point to many others VNets or on-premises.



