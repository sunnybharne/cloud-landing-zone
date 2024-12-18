# Vnet Docs

## Completed pages
- [x] [Virtual Network Documentation](https://learn.microsoft.com/en-us/azure/virtual-network/)
- [ ] About Virtual Network


## Todo
- [ ] [Vnet Training](https://learn.microsoft.com/en-us/training/modules/introduction-to-azure-virtual-networks/?source=recommendations)

## Vnet Basics
- Communication of Azure resources with the internet.
    - public outbound communication is allowed by default
    - Manage public outbound connections using
        - public ip address
        - Nat gateway
        - public loadbalancer
    - Manage inbound connections using
        - public ip address
        - public loadbalancer
    - Assigning internal standard loadbalancer will not provide outboud ability to the vnet

- Communication between Azure resources.
- Communication with on-premises resources.
- Filtering of network traffic.
- Routing of network traffic.
- Integration with Azure services.

## Virtual network service point
- Direct connection to the serverless resources(like private endpoints)
- This is achieved by doing connecting vnets private endpoint to the service directly over azure backbone network.

## Vnet peering 
- Connectes two vnets(even from different region)

## Imp points
- When moving VM from one vnet to another, VM needs to be deleted and created again in the new vnet

