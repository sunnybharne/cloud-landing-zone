## Vm level settings
### Connect
    - Connect
        - rdp on windows machine(port 3389)
        - ssh on linux based machine(port 443)
    - Bastion
        - Deploy baston
        - Bastion needs to be in the same region
        - Bastion needs to be attached to the same vnet
        - Tier
            - Basic
            - Standard(Sharable link)
        - Need a new subnet for the bastion, needs /26 

### Networking
### Settings
    - Disks
        - Swap os disks
            - Host caching
        - Data disks
            - Create and attach a new data disks.
            - Storage type
            - Size (4,8,16,32,64,124,256)
            - Encription
    - Availability + scale
        - Size (select the vm size, vm will restart if its already running)
            - D series --> General purpose
            - E series --> High memory
            - B series --> Burstable(Variable cpu performance) 
            - F series --> High GPU
        - Availability and scaling
            - Availability zones
            - Scaling (vmss)
            - Availabilitu set
