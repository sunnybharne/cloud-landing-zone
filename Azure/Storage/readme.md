# Storage account (Iaas) s3

## Basic
    - Globally unique storage account name.
    - Region specific

## Performance
    - Standard (GPV2) 
        - Storage Types
            - (All types)
        - Redundancy (data does not leave the region)
            - LSR - default, 3 Copies in same datacenter (11 9's))
            - ZRS - 3 copies in different AZ
            - GRS - Extra three copies are added to another region (3 + 3)
            - GZRS - Extra one LRS is added to another region
    - Premium (High performance)
        - Storage Types
            - Block Blobs
            - Page Blobs
            - File Shares
        - Redundancy
            - LZR
            - ZRS

## Storage Type
    - Containers - (Blob, can hold only container blobs, unstructured data )
    - File Shares - SMB or NFS (Linux) , Azure file sync is hybrid approach to file share
    - Queues - messages can be queued or dequeued
    - Tables - entities are added to the tables for data(Like a database)
        - Data is stored with partitionKey = column and rowKey = row

## Advance settings
    - Require secure transfer for RestAPI
    - Enable anonymous access on individual containers
    - Enable storage account key access, SAS token (shared access signature) to access data, You can too login with this in portal 
    - Default to microsoft entra authentication in auzre portal
    - Mininum TLS version
    - Datalake
        - used for big data, can store more that 5 petabytes, hadoop of synaps
    - Enable large file shared(This is becuase the file share are not at 5 TB, to get more storage you have to select this option)

## Access Tier
    - Hot (default)
    - cool (Cheaper storage with more expensive read writes) , stored for minimum 30 days
    - cold (much cheaper storage with more expensive reads and wirtes), stored for minimum of 90 days
    - Archive (offline storage,Cheapest but most expensice reads and writes), stored for minimum of 120 day
        - To access files from the archive tier , files needs to be rehydrated first.
        - You have to set the access tier to archive on file to file basis
    - Lifecycle management can be done for the above
    - Premium storage account
        - no access tiers
        - no lifecycle management

## Networking settings
    - Network connectivity
        - Public 
        - From an address space
        - Disable public access
        - Private links
    - Network routing
        - Microsoft network routing (This tries to be on MS backnbone)
        - Internet Routing (This doesnt)

## Data protection  
    - Recovery
        - Enable point in time restore containers
        - Soft delete for blobs / containers  and files shares
    - Tracking(S3 bucket versioning)
    - Change feed(Keep track of create, modification and delete change to blobs)
    - Immutablitiy (In this file will not be deleted ever)

## Encription
    - Data encrypted by default
    - MMK (Micrososft managed keys)
    - CMK (Customer managed keys)
        when its created you have to decide if this needs to be appled on only blobs or all storage types(Cant be changed afterwords)
    - Enable infrastructure encryption

## Storage account accessibility
    - Storage explorer, downloadable software for viewing the storage services
    - Storage browser is another way of viewing your storage services

------------------------

*Imp points*
    - AZ copy copies the content from one container to another
    - 

*Azure migrate*
    - Discovery (Examins your achitecture and gives a suggestion on migration)

*Azure databox (AWS snowball)*
    - Databox (100 tB)
    - Databox Disk (8 tb)
    - Databox Heavy (1 PB)
