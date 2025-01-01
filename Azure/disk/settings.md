# Disk settings

## Settings

### Configuration
- Enable shared disk
    - This can be enabled for 2 or 3 vm's
    - when this is enabled , host caching is unavailable, 
- Enable demand bursting 
    - Only available for more than 512 gb's,
    - This helps burst iops beyond provisioned target up to 30000 iops and 1000 mb's
    - Allow disk to be used for vm hibernation

### Size + Performance
- Storage type
    - Premium SSD
    - Standard SSD
    - Standard HHD
    - Zone redundant storage
        - Premium SSD
        - Standard SSD
- Disk size
- Performance tier
    - IOPS , MB/s

### Encryption
- Plaform managed keys
- Customer managed keys
- Platform managed and customer managed keys

### Networking
- Public access from all networks
- Enable private access
    - Disk access
        - Private link
- Display public and private access

### Disk Export
- Allow data access with Azure AD authentication
- Generate a secure URL
    - URl expires in ___ seconds

### Properties
- Resource ID
- Other details

### Automation
- CLI/PS
- Task
- Export template
