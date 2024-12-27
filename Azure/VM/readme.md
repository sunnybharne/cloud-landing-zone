# Virtual Machines(VM)

## Vm Creation
    - Redundancy
    - Security type
        - Standard
        - Trusted launch
        - Confidential vertual machine
    - Image
    - Run with spot instances
    - Size
        - D series --> General purpose
        - E series --> High memory
        - B series --> Burstable(Variable cpu performance) 
        - F series --> High GPU
    - Administrator account
        - Username,password
    - Public inbound port
        - None
        - Allow selected ports
            - Http, Https, Ssh, Rdp
    - Disk
        - Os disk (Temporary storage)
            - Premium SSD, Standard SSD, Standard HDD
            - Zone redundant storage
                - Premium SSD, Standard SSD
        - Key management
            - Platform managed keys
            - Customer managed keys
            - Platform and customer managed keys
        - Enable ultra disk (More crazyer than Premium SSD)
        - Data disk for VM 
            - This can be detached and reattached to another vm
            - This cant be attached to two different VM's at the same time (Use file shares to do that)
        

### IP address
    - public IP address is not free , every public IP address has a cost attached to it.
    - Dynamic Public IP address 
    - Static Public IP address
    - Private IP address

### Dedicated host virtual machines
    - Create dedicated host from marketplace
    - Then create virtual machines inside that dedicated host

### Azure Spot instances 
    - The vm's can be stopped any time 
    - Should be used for workloads which can handle vm's stopping , reserved for 1 or 3 years

### Reserved instance 
    - You can reserve capacity in bulk for longer periods of time which can then cost you less 

### Azure monitoring 
    - This helps monitor the logs and other metrics of the virtual machine


## VM Scale sets(VMSS)
    - Scaling based on conditions
    - up to 100 VMs in single scale sets can be increased that to 1000
    - It creates a loadbalancer by default(Should be explicitly deleted)

## Availability sets
    - load balancing between two servers
    - Fault domains (machines running on different rack)
    - Update domains (used for updateing the applications)

## Proximity group
    - Having multiple machines close to each other
    - Faster inter communication due to being very close to each other 

## Imp points
    - RDP - port 3389 windows machine 
    - SSH - port 22 Linux machine 
    - Vent ( free of cost, only traffic going out of the Avnet is charged)
    - Cloud init will run the script at startup
    - NSG ( behaves like a small firewall ), no charges
    - Inbound and outbound rules can be added
    - Disk , charged 
    - Public Ip , charged - traffic from public Internet 
    - Static assignment ( ip address does not change on restart )
    - Dynamic assignment ( ip address changes on restart )
    - Nic ( network interface )
    - One vm should be connected to at least one subnet using NIC(ACL using nsg).
    - Can be assigned to more that one private IP address if there are more than one subnet linked to the VM.
    - Each VM can be assigned one public IP address so that It can be accessed from the internet.


## VM sizes 
    - Bs ( low cost )
    - D general purpose 
    - F more compute power 
    - M more memory 
    - N more gpu power
## Availability chart 
    - Single instance premium ssd or ultra disk 99.9 
    - Single instance standard ssd 99.5
    -  Single instanceHdd 95
## Availability sets ( logical grouping to increase availability) 99.95
    - Fault domain ( grouping on different power source )
    - Update domain ( grouping on the base of updates ) 
## Availablity zones 99.99 
    - Scale set ( create multiple vms ) 
    - Add optional lb
    - Multiple availablity zones 
    - Scaling 
    - Manual scaling 
    - Rule based scaling 
## Pricing:
    - Dedicated host 
    - Azure spot instance ( unused capacity ,azure can decide to take it back ) 
    - Azure reservations ( pay for long term at discount ) 

## Disk storage
    - Connected to azure VM's
        - Standard HDD
        - Standard SSD
        - Premium SSD
        - Ultra disk SSD


