# Describe cloud concepts (25–30%) 

## Describe cloud computing 
### Define cloud computing 
A service that provides computational resources over the internet.

### Describe the shared responsibility model 
A framework which defines the division of responsibilities between the customer and provider.

Always the customer's responsibility:
- Information and Data
- Devices
- Accounts and Identities

Always the cloud provider's responsibility:
- Physical Hosts
- Physical Network
- Physical Datacenter

Service type dependant:
- Identity and Directory Infrastructure
    - IaaS: Customer
    - PaaS: Shared
    - SaaS: Shared
- Applications
    - IaaS: Customer
    - PaaS: Shared
    - SaaS: Cloud Provider
- Network Controls
    - IaaS: Customer
    - PaaS: Shared
    - SaaS: Cloud Provider
- Operating Systems
    - IaaS: Customer
    - PaaS: Cloud Provider
    - SaaS: Cloud Provider

### Define each cloud model and outline their pros, cons and use cases  

**Public**

- A third-party service providing online computational resources

- Physical infrastructure shared between organizations (multi-tenant environment)

- Data and workloads are securely separated between organizations

Pros:
- No upfront payment
- Quick and easy provisioning/deprovisioning of resources
- Only pay for what you use

Cons:
- Less control over resources and security

**Private**

Definition:
- A cloud solution dedicating all infrastructure to a single organization (single-tenant environment)
- It can be on-prem, or provided by a third-party
Pros:
- Complete control over resources and security
- Data is not collocated with others' data
Cons:
- Hardware must be purchased
- You are responsible for hardware maintenance and updates

**Hybrid**

A computing environment that uses both public and private clouds in an inter-connected environment.

- Most flexible option
- You get to pick where your application is run
- Organizations control security, compliance, or legal requirements

Use case:
- Can be used to allow a private cloud to scale for increased, temporary demand by deploying public cloud resources.
- Can be used for an extra layer of security.
   > E.g. Keeping some services on public cloud and others on private cloud infrastructure.

**Multi-Cloud (New)**

An environment where you deal with 2 or more public cloud providers and manage resources and security in both environments.

### Describe the consumption-based model
#### CapEx (Capital Expenditure)
One-time, up-front expenditure or purchase or secure tangible resources.

For Example:
- A new building
- Repaving the parking lot
- Building a datacenter

#### OpEx (Operational Expenditure)
Spending money on services or products over time.
For Example:
- Renting a convention center
- Leasing a company vehicle
- Signing up for cloud services

Cloud computing falls under OpEx.

With Cloud Computing, you don't pay for physical infrastructure, electricity, security, or anything associated with maintaining a datacenter. Instead, you ONLY pay for the IT resources and stop when you don't use them.

Benefits:
- No upfront cost
- No wasted resources
- Pay for what you need
- Stop paying when you don't

### Compare cloud pricing models 
[https://spot.io/resources/azure-pricing/the-complete-guide/]
#### Pay as you go
Pay for services on Azure according to actual usage
- Billed per second
- No long term commitment or upfront payment

Benefits:
- Flexibility to increase/decrease resources as needed
- VMs can be scaled automatically
    
Suitable for:
- Users that prefer flexibility
- Users that prefer to convert capital expenses into operating expenses
- Users that Host applications with volatile/short term workloads

#### Reserved Instances
You can purchase Reserved Virtual Machine Instances (RVMI's) for 1 or 3 years in a specific region
- Can cancel, but there is an early termination fee
- Can replace reserved instances during commitment period
    
Benefits:
- Save up to 72% compared to Pay as you go.

Suitable for:
- Apps with stable ongoing use
- Organizations with a fixed budget
- Large Scale applications where a certain amount of virtual machines are always in use

#### Spot Instances

Unused computing power at a discount.
- Spot instances can be interrupted at short notice. 
- To combat this, you can use Virtual Machine Scale Sets (VMSS). They let you run a group of identical VMs that scale automatically.
    > The evicted VMs can be replaced automatically, creating a more stable environment for your app.

Benefits:
- The discount can reach up to 90% compared to Pay as you go 
      
Suitable for:
- Distributed apps
- Fault tolerant apps
- Stateless apps
- Workloads that aren't urgent
- Heavily parellalized workloads

### Describe serverless 
Definition: A provided infrastructure and runtime environment to deploy applications rapidly.
You don't need to worry about the:
- Infrastructure
- VM Scaling
- VM Provisioning
- VM Management

You manage apps, pay for resources consumed, and stop when the app is idle.

Benefits:
- Helps users focus on development instead of infrastructure
- Only pay for resources you use
- No need to manage servers
- Provides dynamic scalability
- Provides quick deployments and quick updates
- Provides low latency (code runs in the nearest region - closer to the end-user)

Cons:
- Less control over infrastructure
- Unpredictable cost at scale
- Debugging and monitoring may be harder

## Describe the benefits of using cloud services 
[https://learn.microsoft.com/en-us/training/modules/describe-benefits-use-cloud-services/] 

### High availability: 
An app being available regardless of disruptions

When you're architecturing an app, you need to account for service availability guarantees (part of SLAs)

Benefits:
- The higher your app's availability, the more time you save end-users in down-time. They can accomplish more.

Cons:
- The higher the service's availability, the more it will cost to run and keep at a high availability. This will then be more expensive for the end user.


### Scalability:
The ability to adjust resources to meet demand.

Benefits:
- If you experience high traffic, you can add resources to handle it.
- If demand drops, you can use less resources and pay less.

### Reliability
The ability of a system to recover from failure and continue to function.
The cloud allows you to have reliable and resilient infrastructure because it gives you access to deploy resources all around the world.

Benefits:
- If one region has a catastrophic event, the other regions are available to use.

### Predictability 
#### Performance Predictability** 
Because of things like 
- Auto scaling
- Load balancing
- High availability

You can predicting the resources needed to deliver a positive experience for your customers.

#### Cost Predictability:

You can use:
- Total Cost of Ownership (TCO)
- Pricing calculator to predict cost potential

...to can track resource usage in real time and monitor resources to make sure they're being used efficiently.

### Security
Security makes sure your cloud is safe from attacks, with flexibility in how much you manage yourself.

In practice, this means:
- Choice of Control Level: 
    - IaaS      → You manage security patches. 
    - PaaS/SaaS → Azure manages security patches. 

- Tools for protection:
    e.g.:
    - Azure Firewall
    - Security Center
    - Defender

### Governance 
governance ensures your cloud resources stay compliant, consistent, and under control

In practice, this means:
- ARM templates/policies make sure resources are deployed with the right config.
- Compliance & Audit tools scan your environment for resources that don’t meet standards:
    - Azure Policy
    - Blueprints
- Automatic Updates to Standards across the whole cloud environment.
- Centralized Management over who can deploy what, where, and how.

### Describe the benefits of manageability in the cloud 
Manageability is how you manage your cloud resources.

In practice:
- Automatic resource scaling
- Deploy from templates
- Health monitoring
- Alerts

## Describe cloud service types 
[https://www.bigcommerce.co.uk/articles/ecommerce/saas-vs-paas-vs-iaas/]
### Define and outline the examples, use cases and responsibilities of:
#### Infrastructure as a Service (IaaS)
IaaS provides virtualized computing resources over the internet, such as servers, storage, and networking, allowing users to run applications without buying physical hardware.

Examples:
- Azure Virtual Machines
- Azure Virtual Network
- Azure Load Balancer

Advantages:
- Full control over infrastructure and operating systems
- Highly scalable and flexible for various workloads
- Pay-as-you-go pricing reduces upfront costs
- Ideal for hosting legacy applications or custom environments

Disadvantages:
- Requires technical expertise to manage and maintain
- Users are responsible for updates, patches, and security
- Can become costly if not properly optimized

#### Platform as a Service (PaaS)
PaaS lets you build, deploy, and manage applications without managing infrastructure like servers or storage.

Primarily Used By:
- Developers building software or applications

Examples:
- Azure Functions – Serverless compute
- Azure SQL Database – Managed relational database
- Azure Kubernetes Service (AKS)

Advantages:
- Developers don’t need to start from scratch — saves time and money
- Built-in tools for deployment, scaling, and monitoring
- Supports rapid development and continuous integration
- Reduces infrastructure management overhead

Disadvantages:
- Limited control over underlying infrastructure
- May not support all legacy or custom applications
- Risk of vendor lock-in due to proprietary services

#### Software as a Service (SaaS)
SaaS platforms deliver software applications over the internet, managed by a third-party provider.

Examples:
- Microsoft 365
- Microsoft Teams

Advantages:
- No need to install or maintain software locally
- Accessible from anywhere with internet
- Centralized platform for teams and organizations
- Easy role-based access and automatic updates
- Subscription-based pricing

Disadvantages:
- Data security concerns due to third-party hosting
- Limited customization and integration options
- Less control over performance, features, and data handling

# Describe Azure architecture and services (35–40%) 
## Describe the core architectural components of Azure
### Describe Azure regions
[https://idodata.com/2025/05/06/az-900-describe-azure-regions-region-pairs-and-sovereign-regions/]

A specific geographic area that contains one or more data centers.

Each region offers redundancy, scalability, and availability for Azure services.

Advantage:
- Regions help businesses meet data residency requirements, such as regulations requiring data to remain within a specific geographic boundary (e.g., Europe).

### Region Pairs
Azure pairs each region with another region in the same geography, typically at least 300 miles apart. This strategy is known as a region pair.

Benefits:
- Region pairs are designed to enhance high availability and disaster recovery:
- If one region fails or is affected by an outage, services can failover to the paired region.

In the event of a geographic disaster affecting both regions, Azure prioritizes recovery for one of them.

Planned updates are intentionally not deployed simultaneously to both regions in a pair to reduce risk.

### Sovereign regions
Specially isolated Azure environments designed to meet strict national and governmental requirements.

1. United States Sovereign Regions
2. China Sovereign Regions
3. Germany Sovereign Region

### Describe Azure datacenters
[https://idodata.com/2025/05/08/az-900-describe-azure-datacenters/]

An Azure datacenter is a physical building that contains large numbers of networked computer servers.

Each datacenter is located in a specific geographic location, chosen based on accessibility, climate stability, and regional demand.

Azure datacenters are designed to be self-sufficient, each with its own power supply, cooling systems, and network infrastructure.

Resources are not shared between datacenters, helping to reduce the risk of systemic failure.


### Describe availability zones
[https://learn.microsoft.com/en-us/azure/reliability/availability-zones-overview?tabs=azure-cli]

An availability zone is a logical grouping of one or more physically separate datacenters within a region.

Each availability zone is built in a way that if something goes wrong in one (like a power outage or network issue), the others keep working.

A single datacenter doesn’t offer this level of protection on its own.

Each availability zone has independent:
- Power
- Cooling
- Networking infrastructure.

Generally, thay're separated by several kilometers, and within 100 kilometers of each other.
- Close enough for low-latency connections to other availability zones.
- Far enough apart to reduce the chance more than one will be affected by local outages/weather.

Example Azure regions:

(regions 1 supports availability zones, region 2 doesn't have availability zones)
```
├── Azure Region 1
│   ├── Availability Zone 1
│   │   └── Datacenter(s)
│   ├── Availability Zone 2
│   │   └── Datacenter(s)
│   └── Availability Zone 3
│       └── Datacenter(s)
└── Azure Region 2
    └── Datacenter(s)
```

### Resources:
An Azure resource is any manageable item available through Azure.

Examples:
- Virtual Machines (VMs)
- Storage Accounts
- Web Apps
- Databases
- Virtual Networks

Resources are created, deployed, and managed using tools like the Azure Portal, CLI, PowerShell, or ARM templates.

Each resource has properties like location, type, and pricing tier.

### Azure Solution:
A conceptual bundle of services and resources designed to solve a specific business or technical need.

Example:

A web hosting solution might include App Service, SQL Database, Key Vault, and CDN.

### Resource Groups:
A container that holds related Azure resources for a solution.
Example: You might place all the resources from your web hosting solution into one resource group.

The resource group can include all the resources for the solution or only resources that you want to manage as a group.
You decide how to allocate resources to resource groups based on what makes the most sense for your organization.

Generally, resources sharing the same lifecycle share a resource group so it's easier to deploy, update, and delete them as a group.

The Azure portal uses the resource group scope to create views that span across multiple resources. For example:

**Metrics blade**

- Metrics info like CPU/resources.

**Deployments blade**

- ARM template/Bicep deployment history of that resource group (includes portal deployments).

**Policy blade**

- Info related to policies enforced on the resource group.

**Diagnostics settings blade**

- Errors/warnings to review.

The resource group stores metadata about the resources.

Specifying a location for the resource group dictates where that metadata is stored.

For compliance reasons, you might need to ensure that your data is stored in a particular region.

Resources inside a resource group can be in different regions.

### Management groups
[https://learn.microsoft.com/en-us/azure/governance/management-groups/overview]

Management groups provide a scalable way to manage access, policies, and compliance across multiple Azure subscriptions. They offer a governance scope above subscriptions, enabling centralized control and consistency.

Key Features:
- Governance Inheritance: Policies + access controls applied to a management group automatically cascade to all child groups and subscriptions.
- Enterprise-Grade Management: Supports large-scale environments, regardless of subscription type.
- Microsoft Entra Integration: All subscriptions within a management group must be associated with the same Microsoft Entra tenant.

Example:

You can apply a policy at the management group level to restrict VM creation to specific regions.
This policy will automatically apply to all nested management groups, subscriptions, and resources.

**Governance Hierarchy**

Management groups allow you to build a hierarchical structure that mirrors your organization’s needs.
Example:
```

                  ┌───────────────────────────┐   ┌───────────────────────────────┐
                  │   👥 MANAGEMENT GROUPS    │   │   🔑 SUBSCRIPTIONS            │
Tenant Root Group │                           │   │                               │
└─────────────────┼── Contoso                 │   │                               │
                  │   ├── Platform            │   │                               │      
                  │   │   ├── Management      │   │                               │      
                  │   │   │   └───────────────┼───┼── Management Subscription     │      
                  │   │   ├── Connectivity    │   │                               │      
                  │   │   │   └───────────────┼───┼── Connectivity Subscription   │      
                  │   │   ├── Identity        │   │                               │      
                  │   │   │   └───────────────┼───┼── Identity Subscription       │      
                  │   ├── │Landing Zones      │   │                               │      
                  │   │   ├── SAP             │   │                               │      
                  │   │   ├── Corp            │   │                               │      
                  │   │   │   ├───────────────┼───┼── Landing Zone A1             │      
                  │   │   │   └───────────────┼───┼── Landing Zone A2             │      
                  │   │   ├── Online          │   │                               │      
                  │   ├── Decommissioned      │   │                               │      
                  │   │   └───────────────────┼───┼── Decommissioned Subscription │      
                  │   └── Sandbox             │   │                               │      
                  │       ├───────────────────┼───┼── Sandbox Subscription 1      │      
                  │       └───────────────────┼───┼── Sandbox Subscription 2      │      
                  └───────────────────────────┘   └───────────────────────────────┘      
```


### Subscriptions
[https://www.alifconsulting.com/post/azure-subscription]

An Azure subscription is a logical container used to provision resources in Azure.
It holds the details of all resources.

You can identify each resource by the subscription it belongs to.
As the VM is used, VM usage is aggregated and billed monthly. 

Boundaries:
1. Billing boundary
    - Defines billing requirements for accessing resources.
    - Each subscription has a separate billing so that multiple subscriptions can be created as per business needs. 
2. Access control boundary 
    - To separate subscriptions and apply different management policies, an access control boundary can be constructed at the subscription level. This helps represent diverse organizational structures and enforce governance effectively.
    - An Access Control Boundary is not a resource.
    - It’s a security and governance boundary, typically applied at the subscription level.
    - It’s enforced through settings like:
        - Role-Based Access Control (RBAC): Who can do what
        - Azure Policy: What can be done and how
        - Resource locks and tags: Additional governance tools

### Azure Hierarchy Example
```
└── Business Unit
    └── Geography (e.g., England)
        ├── Environment (e.g., Production)
        │   └── Management Group
        │       ├── Subscription A  ← [Access Control Boundary + Billing Boundary can be added]
        │       │   ├── Resource Group 1
        │       │   │   ├── Storage Account
        │       │   │   │   ├── Blob Containers
        │       │   │   │   │   └── Blobs (files)
        │       │   │   │   ├── File Shares
        │       │   │   │   │   └── Files & Directories
        │       │   │   │   ├── Queues
        │       │   │   │   │   └── Messages
        │       │   │   │   ├── Tables
        │       │   │   │   │   └── Entities
        │       │   │   │   └── Data Lake Gen2 (if enabled)
        │       │   │   │       └── File System
        │       │   │   │       └── Directories & Files
        │       │   │   ├── Resource: Virtual Machine
        │       │   │   └── Resource: Virtual Network
        │       │   └── Resource Group 2
        │       │       ├── Resource: Azure SQL Database
        │       │       └── Resource: Azure Function
        │       └── Subscription B  ← [Access Control Boundary + Billing Boundary can be added]
        │           └── Resource Group 3
        │               ├── Resource: Web App
        │               └── Resource: Key Vault
        └── Environment (e.g., Non-Production)
            └── Management Group
                └── ...
```

## Describe Azure storage services 
### Compare Azure Storage services 
[https://learn.microsoft.com/en-us/azure/architecture/guide/technology-choices/storage-options]

Azure Storage is a managed service for providing cloud storage.
Storage in Azure is highly available, secure, durable, scalable, and redundant.

#### 🧱 [ Core Storage Services ]
These are the foundational storage types in Azure:

**Azure Blob Storage:**

An object storage solution for the cloud.  
Optimized for storing massive amounts of unstructured data.

Use Cases:
- Serving images or documents directly to a browser.
- Storing files for distributed access.
- Streaming video and audio.
- Writing to log files.
- Storing data for backup and restore, disaster recovery, and archiving.
- Storing data for analysis by an on-premises or Azure-hosted service.

**Azure Files:**

Azure Files provides fully managed, native SMB (Server Message Block) and NFS (Network File System) file shares, without the need to run a virtual machine.

You can mount an Azure file share as a network drive to any Azure virtual machine or on-premises computer.

**Azure disk storage:**

Azure disk storage offers persistent, high-performance block storage to power Azure Virtual Machines.

Offer the industry's only single-instance, service-level agreement (SLA) for virtual machines that use Azure Premium SSD or Azure Ultra Disk Storage.

Azure manages disks as a top-level resource.

Properties of Azure Disks:
- Highly durable
- Secure
- high availability:
> Provides availability sets and availability zones for your Azure Virtual Machines fault domains.

Azure Resource Manager (ARM) capabilities are provided by default, including:
- Azure Role-Based Access Control (RBAC): Assigns fine-grained permissions to users, groups, and applications for managing resources securely.
- Policies: Enforces rules and compliance standards across your Azure environment.
- Tagging: Adds metadata labels to resources for better organization, cost tracking, and automation.

**Data Lake Storage Gen2**

Data Lake Storage Gen2 is Blob Storage with a hierarchical file system.

This hierarchical structure enables:
- Efficient file operations (like rename and delete)
- Directory-level access control
- Optimized performance for big data analytics

Includes:
- Low-cost tiered storage
- High availability
- Strong consistency
- Disaster recovery capabilities

Use Cases:
- Big data analytics with Hadoop/Spark


#### 🔄 [ Integration & Sync Tools ]
These services extend or connect core storage:

**Azure File Sync**

For centralizing file shares in Azure Files.
Azure File Sync offers the flexibility, performance, and compatibility of an on-premises file server.

Works With Azure Files

**Azure Data Box**

A solution that allows for offline, bulk data transfer in and out of Azure using a physical storage appliance.
It's used when network-based data transfer is constrained by:
- Time
- Network availability
- Cost

Works With:
- Blob
- Files
- Disks

**Data Box Gateway**

A storage solution that enables you to seamlessly send data to Azure.

It's a virtual device based on a virtual machine provisioned in your virtualized environment/hypervisor.

The virtual device is on-premises and you write data to it by using the NFS and SMB protocols.

The device then transfers your data to:
- Azure block blobs
- Page blobs
- Azure Files.

#### 🚀 [ Advanced & Specialized Storage ]
These are optimized for performance, container workloads, or HPC (High-Performance Computing):

**Azure NetApp Files**

A file storage service that's:
- enterprise-class
- high-performance

Supports any workload type and is highly available by default.

You can select service and performance levels and set up snapshots through the service.

Use Cases:
- SAP
- Oracle
- HPC

**Azure Managed Lustre**

A high-performance distributed parallel file system solution.
ideal for HPC workloads that require high throughput and low latency.
Use Cases:
- AI/ML
- genomics

**Azure Container Storage**

A volume management + deployment + orchestration service that is:
- Fully managed
- Cloud-based
- Built natively for containers.
    
It integrates with Kubernetes
- Allows you to dynamically + automatically provision persistent volumes to store data for stateful applications running on Kubernetes clusters.

#### 📡 [ Edge & Hybrid Solutions ]
These bring Azure Storage closer to your location:

**Azure Stack Edge**

An on-prem network device that moves data into and out of Azure.
Has AI-enabled edge compute to pre-process data during upload.

(Data Box Gateway is a virtual version of the device but with the same data transfer capabilities)

Use Cases:
- Local inference
- data preprocessing

### Describe storage tiers 
[https://learn.microsoft.com/en-us/azure/storage/blobs/access-tiers-overview]

To manage costs for expanding storage needs, it can be helpful to organize data based on access frequency and retention time.

Different access tiers exist so blob data can be stored cost-effectively based on its usage.

Azure Storage access tiers:
1. Hot tier
    - Online
    - Optimized for storing data with high access/modification frequency
    - Highest storage costs
    - Lowest access costs
2. Cool tier
    - Online
    - Optimized for storing data with low access/modification frequency
    - Data should be stored for a minimum of 30 days
    - Compared to the hot tier:
        - Lower storage costs
        - Higher access costs
3. Cold tier
    - Online
    - Storing data with:
        - Low access/modification frequency
        - Requires fast retrieval
    - Should be stored for a minimum of 90 days
    - Compared to the cool tier: 
        - Lower storage costs
        - Higher access costs
4. Archive tier
    - Offline
    - Optimized for storing data that:
        - Low access frequency
        - Latency requirements are relaxed (e.g., hours rather than seconds or minutes)
    - Should be stored for a minimum of 180 days

Azure storage capacity limits are set at the account level, rather than according to access tier.

You can choose to maximize your capacity usage in one tier, or to distribute capacity across two or more tiers.

### Storage Accounts  
A storage account contains Azure Storage data objects:
- Blobs
- Files
- Queues
- Tables

The storage account provides a unique namespace for your Azure Storage data that's accessible from anywhere in the world over HTTP or HTTPS.

Data in your storage account is durable and highly available, secure, and massively scalable.

### Storage Types

#### Standard general-purpose v2
Supported Storage Services:
- Blob Storage (including Data Lake Storage)
- Queue Storage
- Table Storage
- Azure Files

Redundancy Options:
- Locally redundant storage (LRS)
- Geo-redundant storage (GRS)
- Read-access geo-redundant storage (RA-GRS)
- Zone-redundant storage (ZRS)
- Geo-zone-redundant storage (GZRS)
- Read-access geo-zone-redundant storage (RA-GZRS)

Usage:
- Standard storage account type for blobs, file shares, queues, and tables.
- Recommended for most scenarios using Azure Storage.
- For NFS support in Azure Files, use the premium file shares account type.

#### Premium block blobs
Supported Storage Services:
- Blob Storage (including Data Lake Storage)

Redundancy Options:
- Locally redundant storage (LRS)
- Zone-redundant storage (ZRS)

Usage:
- Premium storage account type for block blobs and append blobs.
- Recommended for scenarios with high transaction rates, smaller objects, or consistently low storage latency.

#### Premium file shares
Supported Storage Services:
- Azure Files

Redundancy Options:
- Locally redundant storage (LRS)
- Zone-redundant storage (ZRS)

Usage:
- Premium storage account type for file shares only.
- Recommended for enterprise or high-performance scale applications.
- Supports both Server Message Block (SMB) and NFS file shares.

#### Premium page blobs
Supported Storage Services:
  - Page blobs only
  
Redundancy Options:
- Locally redundant storage (LRS)
- Zone-redundant storage (ZRS)

Usage:
- Premium storage account type for page blobs only.
- Learn more about page blobs and sample use cases.


### Describe redundancy options 
Azure Storage always stores multiple copies of your data to protect it from planned/unplanned events.

Examples of these events:
- Transient hardware failures
- Network or power outages
- Massive natural disasters

Redundancy ensures that your storage account meets its availability and durability targets even in the face of failures.

Finding the right redundancy option boils down to tradeoffs between lower costs + higher availability.

Factors to determine the right redundancy option:
- How is your data replicated within the primary region?
- Geo-replication: Is data replicated from a primary region to a second, geographically distant region, to protect against regional disasters? 
- Geo-replication with read access: Does your application need read access to the replicated data in the secondary region during an outage in the primary region?

The services that comprise Azure Storage are managed through a common Azure resource called a storage account.

The storage account represents a shared pool of storage that can be used to deploy storage resources such as:
- Blob containers (Blob Storage)
- File shares (Azure Files)
- Tables (Table Storage)
- Queues (Queue Storage)
    
#### Redundancy Options in Azure Storage:

Locally Redundant Storage (LRS)
- Data is replicated three times within a single data center in one region.
- Lowest cost option.
- Protects against hardware failures but not data center outages.

Zone-Redundant Storage (ZRS)
- Data is synchronously replicated across three Azure availability zones within one region.
- Offers higher availability and durability than LRS.
- Protects against zone-level failures.

Geo-Redundant Storage (GRS)
- Data is replicated to a secondary region hundreds of miles away from the primary region.
- Asynchronous replication.
- Protects against regional outages but read access to secondary is not available by default.

Read-Access Geo-Redundant Storage (RA-GRS)
- Same as GRS, but allows read access to the secondary region.
- Useful for applications that need high availability even during regional outages.

Geo-Zone-Redundant Storage (GZRS)
- Combines ZRS in the primary region with asynchronous replication to a secondary region.
- Offers both zone-level and regional protection.

Read-Access Geo-Zone-Redundant Storage (RA-GZRS)
- Same as GZRS, but includes read access to the secondary region.
- Ideal for mission-critical applications requiring maximum availability.

### Identify options for moving files, including AzCopy, Azure Storage Explorer, and Azure File Sync 
#### AzCopy
AzCopy is a command-line utility that you can use to copy files to or from a storage account.

#### Azure Storage Explorer
A desktop application that helps manage your Azure Blob Storage and Azure Data Lake storage.

#### Azure File Sync
A service for centralizing an organization's file shares in Azure Files while keeping the flexibility, performance, and compatibility of a Windows file server.

You can opt to keep a full copy of your data locally.

OR

You can transform Windows Server into a quick cache of an Azure file share

You can use any protocol that's available on Windows Server to access your data locally, including:
- Server Message Block (SMB)
- Network File System (NFS)
- File Transfer Protocol over SSL/TLS (FTPS)

You can have as many caches as you need across the world.


### Describe migration options, including Azure Migrate and Azure Data Box 

#### Azure Migrate
Built for lifting and shifting workloads (e.g., SQL Server to an Azure Virtual Machine)

Provides a centralized hub to start, execute, and track your migration process.

Capabilities:
- Can see and assess your on-premises infrastructure.
- Can works across your entire data estate.
- Gives deployment recommendations for Azure SQL-based options.
- Offers target sizing guidance to help right-size your Azure resources.
- Provides monthly cost estimates.
- Provides insights before you move anything.

#### Azure Data Box
Built for massive data transfers that are not feasable do over the internet.

This is a physical device shipped to you by Microsoft.

Ideal for:
- multi-terabyte datasets
- environments with limited connectivity.

How it works:
1. You copy your data onto the device locally.
2. Microsoft then securely transfers the data to Azure on your behalf.

Data Box supports:
- Bulk data migration
- Disaster recovery data import
- Offline transfers where privacy and bandwidth are concerns

## Describe Azure identity, access, and security 
### Describe directory services in Azure, including Microsoft Entra ID and Microsoft Entra Domain Services 
[https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/2-directory-services]

#### Microsoft Entra ID
Microsoft's cloud-based identity and access management service.
Can also help you maintain your on-premises Active Directory deployment.

Responsibilities:
- identity accounts - controlled by user
- Global availability - controlled by Microsoft

When you connect Active Directory with Microsoft Entra ID, Microsoft detects suspicious sign-in attempts.

Use Cases:
- IT administrators: For controlling access to applications + resources based business requirements.
- App developers: To get a standards-based approach for adding functionality to applications that they build. E.g.:
    - SSO (Single Sign on) functionality
    - Enabling an app to work with a user's existing credentials.
- Users: Can manage their identities and take maintenance actions like self-service password reset.
- Online service subscribers: Authentication provided by Microsoft 365, Microsoft Office 365, Azure, etc is Microsoft Entra ID.

**Services provided by Microsoft Entra ID:**

**Authentication** 

Includes:
- Verifying identity to access applications and resources
- Self-service password reset
- Multifactor authentication
- Custom list of banned passwords
- Smart lockout services.

**Single sign-on**
- Enables you to remember only one username and one password to access multiple applications.
- A single identity is tied to a user, which simplifies the security model.
- As users change roles or leave an organization, access modifications are tied to that identity, which greatly reduces the effort needed to change or disable accounts.


**Application management**

You can manage your cloud and on-premises apps by using Microsoft Entra ID. Features like Application Proxy, SaaS apps, the My Apps portal, and single sign-on provide a better user experience.

**Device management**

Along with accounts for individual people, Microsoft Entra ID supports the registration of devices. Registration enables devices to be managed through tools like Microsoft Intune. It also allows for device-based Conditional Access policies to restrict access attempts to only those coming from known devices, regardless of the requesting user account.

**Microsoft Entra Connect**

Microsoft Entra Connect connects Microsoft Entra ID with an on-premises AD.
Capabilities:
- Synchronizes user identities between on-premises Active Directory and Microsoft Entra ID.
- Synchronizes changes between both identity systems, so you can use features like
    - SSO
    - Multifactor authentication
    - Self-service password reset under both systems

**Microsoft Entra Domain Services**

A service that provides managed domain services such as:
- Domain join
- Group policy
- Lightweight directory access protocol (LDAP)
- Kerberos/NTLM authentication

A Domain managed by Microsoft Entra Domain Services lets you run legacy applications in the cloud

When you create a Microsoft Entra Domain Services managed domain, you define a unique namespace. This namespace is the domain name. Two Windows Server domain controllers are then deployed into your selected Azure region. This deployment of DCs is known as a replica set.

Azure handles the management, configuration, and updates of these DCs as part of the managed domain.

This includes:
- Backups
- Encryption at rest using Azure Disk Encryption

A managed domain performs a one-way synchronization from Microsoft Entra ID to Microsoft Entra Domain Services.

Resources can be made directly in the managed domain, but aren't synchronized back to Microsoft Entra ID.

In a hybrid environment with an on-premises AD DS environment, Microsoft Entra Connect synchronizes identity information with Microsoft Entra ID, which is then synchronized to the managed domain.

Diagram of Microsoft Entra Connect Sync synchronizing information back to the Microsoft Entra tenant from on-premises AD.

```
                        Automatic Background
                        Sync to your managed
                        domain
┌───────────────────┐                           Microsoft       
│  Virtual Network  │   <────────────────────── Entra ID   <────────────────> On-prem AD
└───────────────────┘    - Sync Users           Tenant      - Sync Users
    Managed Domain       - Groups                           - Groups     
                         - Passwords                        - Passwords  
                         - SIDs to ID                       - SIDs to ID 
                                                    
```

Applications, services, and VMs in Azure connected to a managed domain can use Microsoft Entra Domain Services features such as:
- Domain join
- Group policy
- LDAP
- Kerberos/NTLM authentication

### Describe authentication methods in Azure, including single sign-on (SSO), multi-factor authentication (MFA), and passwordless 
[https://learn.microsoft.com/en-us/training/modules/describe-azure-identity-access-security/3-authentication-methods]

Supported Azure authentication methods:
- Standard passwords
- Single sign-on (SSO)
- Multifactor authentication (MFA)
- Passwordless.

#### Single sign-on (SSO)
Enables a user to sign in one time and use that credential to access multiple resources and applications from different providers.

More identities mean more passwords to remember and change. The more passwords a user has to manage, the greater the risk of a credential-related security incident.

More strain is also placed on help desks to manage all those identities:
- Frequent Account lockouts + password resets
- Tracking down identities of users that left the orgainsation and ensuring they're disabled can be challenging. A small mistake might allow access that should have been removed.

With SSO, access across applications is granted to a single identity that's tied to the user.
Using SSO for accounts makes it easier for users to manage their identities and for IT to manage users.

**NOTE:** SSO is only as secure as the initial authenticator - the subsequent connections are all based on the initial authenticator's security.

#### Microsoft Entra multifactor authentication
Enables users to choose an additional form of authentication during sign-in.

#### Passwordless authentication
The password is removed and replaced with:

`something you have + something you know / something you are`

Setup:
- Register/enroll your device - Azure now knows that it’s associated with you.
- Set up PIN/fingerprint

People are more likely to comply when it's easy and convenient.

Passwordless auth options:
1. Windows Hello for Business
    - The biometric and PIN credentials are directly tied to the user's PC
    - Ideal for information workers that have their own designated Windows PC.
    - A convenient method for seamlessly accessing corporate resources securely.

2. Microsoft Authenticator app

    A convenient multifactor authentication option in addition to a password.
    - You can also use the Authenticator App as a passwordless option.

3. FIDO2 security keys

    The FIDO (Fast IDentity Online) Alliance helps promote open authentication standards and reduce the use of passwords as a form of authentication.
FIDO2 is the latest standard that incorporates the web authentication (WebAuthn) standard.

    FIDO2 security keys are an unphishable standards-based passwordless authentication method that can come in any form factor.

    - FIDO allows sign-in without a username or password via:
        - An external security key
        - A platform key built into a device.
    - FIDO2 security keys can be:
        - USB devices
        - Bluetooth
        - NFC

    With a hardware device that handles the authentication, the security of an account is increased as there's no password that could be exposed or guessed.

### Describe external identities in Azure, including business-to-business (B2B) and business-to-customer (B2C) 
An external identity is a person, device, service, etc. outside your organization.

Microsoft Entra External ID refers to all the ways you can securely interact with users outside of your organization.

Examples:
- For collaborations with partners, distributors, suppliers, or vendors, you can share your resources and define how your internal users can access external organizations.
- If you're a developer creating consumer-facing apps, you can manage your customers' identity experiences.

With External Identities, the external user’s identity provider manages their identity, and you manage access to your apps with Microsoft Entra ID/Azure AD B2C to keep your resources protected.

Diagram showing B2B collaborators accessing your tenant and B2C collaborators accessing the AD B2C tenant.

```
┌─────────────────────────────────────────────────────────────┐
│             External Identity Integration in Azure          │
└─────────────────────────────────────────────────────────────┘

┌─────────────────────────────┐
│       B2B Collaboration     │
├─────────────────────────────┤
│ Partners, Vendors, etc.     │
└────────────┬────────────────┘
             │
┌────────────┴────────────────────────┐
│ Invite or Self-Service Sign-Up      │
└────────────┬────────────────────────┘
             │
┌────────────┴────────────────┐
│ Microsoft Entra External ID │
└────────────┬────────────────┘
             │
┌────────────┴─────────────┐
│       Your Tenant        │
│   (Azure Services)       │
└──────────────────────────┘

─────────────────────────────────────────────────────────────

┌─────────────────────────────┐
│         Azure AD B2C        │
├─────────────────────────────┤
│       App Consumers         │
└────────────┬────────────────┘
             │
┌────────────┴────────────────────────┐
│   User Flows / Custom Policies      │
└────────────┬────────────────────────┘
             │
┌────────────┴─────────────┐
│     Azure AD B2C Tenant  │
│     (Azure Services)     │
└──────────────────────────┘
```

The following capabilities make up External Identities:
1. Business to business (B2B) collaboration

    Letting external users use their preferred identity to sign-in to your Microsoft apps as guests.

2. B2B direct connect

    A mutual, two-way trust with another Microsoft Entra organization for seamless collaboration.
    - Supports Teams shared channels (external users can access your resources from their home instances of Teams)
    - B2B direct connect users aren't represented in your directory, only from the Teams shared channel.

3. Microsoft Azure Active Directory business to customer (B2C)

    Publish apps to consumers while using Azure AD B2C for identity and access management.

Microsoft Entra B2B feature enables guest users from other tenants to be invited by administrators/other users.


Example:
1. The guest/decision maker participates in an access review
2. They attest to the guests' access
3. Reviewers give input on the user's need for continued access, based on Microsoft Entra ID suggestions.
4. When an access review is finished, access changes can be made for guests who don't need it.

### Describe Microsoft Entra Conditional Access 
A tool used by Microsoft Entra ID to allow/deny access to resources based on identity signals.
These signals include:
- Who the user is
- Where the user is
- What device the user is requesting access from.

During sign-in, Conditional Access will:
1. Collect signals from the user
2. Make decisions based on those signals
3. Enforce that decision by either:
    - Allowing/denying the access request
    - Challenging for a multifactor authentication response

Conditional Access helps:

- Empower users to be productive wherever and whenever.
- Protect the organization's assets.
- Provide a more granular multifactor authentication experience for users.

    For example:
    - If a user is at a known location, Second authentication factor won't be prompted.
    - If a user's sign-in signals are unusual/they're at an unexpected location, Second authentication factor will be prompted. 

Conditional Access is useful when you need:

- Multifactor authentication (MFA) to access an application depending on the requester’s role, location, or network.

    E.g., If admins require MFA but not external/regular users.
- Access to services only through approved client applications.

    E.g., Limiting which email applications can connect to your email service.
- Users to access your application only from managed devices.
- Access from untrusted sources blocked.

### Describe Azure role-based access control (RBAC) 
Instead of defining/updating the detailed resource access requirements for each individual across multiple IT/engineering teams manually, Azure role-based access control (Azure RBAC) is used to control access from a centralized location.

There are built-in roles describing common access rules for cloud resources.
Custom roles can also be defined.
All roles have access permissions that relate to that role.
When individuals or groups get assighed to 1+ roles, they receive all the associated access permissions.

1. A new engineer is hired.
2. They are added to an Azure AD security group (e.g., “Engineers”).
3. That group has been assigned an Azure RBAC role (or roles) at a specified scope (such as a subscription, resource group, or set of resources).
4. The new engineer automatically inherits the same access as the other engineers.
5. If an additional resource is added within the same scope, everyone in the group will automatically have the permissions for the new resource.

Role-based access control is applied to a scope, which is a resource/set of resources that this access applies to.

The following diagram shows the relationship between roles and scopes: 

![Role Based Access Scope Diagram][role-based-access-scope-diagram]

[role-based-access-scope-diagram]: https://github.com/Marko-Obradovic/azure-notes/blob/main/images/role-based-access-scope-diagram.png

Azure RBAC is hierarchical — permissions granted at a parent scope automatically apply to all child scopes:

```
Azure RBAC Hierarchy
====================

Management Group (Parent Scope)
│
├── Owner Role → Full control of all child scopes
│   │
│   ├── Subscription A
│   │   ├── Resource Group 1
│   │   │   ├── Resource A
│   │   │   └── Resource B
│   │   └── Resource Group 2
│   │       └── Resource C
│   │
│   └── Subscription B
│       └── (All resources within)
│
└── Reader Role (assigned at Subscription scope)
    │
    └── Members can *view*:
        ├── All Resource Groups
        │   └── Their Resources
        └── But cannot modify them

```

Azure RBAC is enforced on any action initiated against an Azure resource that passes through Azure Resource Manager.
> Resource Manager is a management service that provides a way to organize and secure your cloud resources.

Resource Manager can be accessed from:
- The Azure portal
- Azure Cloud Shell
- Azure PowerShell
- Azure CLI

Azure RBAC doesn't enforce access permissions at the application/data level. Application security must be handled by your application.

Azure RBAC uses an allow model. When you're assigned a role, Azure RBAC allows you to perform actions within that role's scope. If a role assignment grants you READ permissions to a resource group and another grants you WRITE permissions to it, you have both read and write permissions on that resource group.

### Describe the concept of Zero Trust 
Zero Trust starts with the idea that your systems might already be compromised. Because of that, it treats every access request as untrusted and requires verification each time.

**Context:**
> Traditionally, corporate networks were restricted, protected, and generally assumed safe. Only managed computers could join the network, VPN access was tightly controlled, and personal devices were frequently restricted or blocked.

> Instead of assuming that a device is safe because it’s within the corporate network, it requires everyone to authenticate. Then grants access based on authentication rather than location.

Zero Trust Guiding Principles:

- Verify explicitly - Always authenticate and authorize based on all available data points.
- Use least privilege access:
    - Limit user access with Just-In-Time/Just-Enough-Access (JIT/JEA)
    - Risk-based adaptive policies
    - Data protection
- Assume breach - Minimize blast radius and segment access.
- Verify end-to-end encryption.
- Use analytics to get visibility, drive threat detection, and improve defenses.


![Zero Trust Diagram][zero-trust-diagram]

[zero-trust-diagram]: https://github.com/Marko-Obradovic/azure-notes/blob/main/images/zero-trust-diagram.png

### Describe the purpose of the defense-in-depth model 

Objective of defense-in-depth: Protect information + prevent it from being stolen by unauthorized users.

A defense-in-depth strategy uses a series of mechanisms to slow the advance of an attack that aims at acquiring unauthorized access to data.

🧱 **Layers of defense-in-depth**

You can visualize defense-in-depth as a set of layers, with the data to be secured at the center and all the other layers functioning to protect that central data layer.

```
Physical Security/
└── Identity & Access/
    └── Perimeter/
        └── Network/
            └── Compute/
                └── Application/
                    └── Data
```


Each layer provides protection so that if one layer is breached, a subsequent layer is already in place to prevent further exposure.

It slows down an attack and provides alert information that security teams can act upon, either automatically or manually.

High Level Overview of each layer's role:
1. Physical security layer: Protects computing hardware in the datacenter.
2. Identity and access layer: Controls access to infrastructure and change control.
3. Perimeter layer: Protects against DDoS Attacks.
4. Network layer: Limits communication between resources through segmentation and access controls.
5. Compute layer: Secures access to virtual machines.
6. Application layer: Ensures application security.
7. Data layer: Controls business and customer data access.

These layers provide a guideline for you to help make security configuration decisions in all of the layers of your applications.

More detailed overview of each layer:

#### Physical security
- Physically securing access to buildings
- Controlling access to computing hardware within the datacenter are the first line of defense.

#### Identity and access

At this layer, it's important to:

- Secure identities:
    - Control access to infrastructure and change control.
    - Access is granted only to what's needed
- Use single sign-on (SSO) and multifactor authentication.
- Audit events and changes: Sign-in events/changes are logged 

#### Perimeter
Protects from network-based attacks against your resources
- Identifies these attacks
- Eliminates their impact
- Alerts when they happen

At this layer, it's important to:
- Use DDoS protection to filter large-scale attacks before they can affect the availability of a system for users.
- Use perimeter firewalls to identify and alert on malicious attacks against your network.

#### Network
Limits network connectivity across all resources to allow only what's required.
By limiting this communication, you reduce the risk of an attack spreading to other systems in your network.

At this layer, it's important to:

- Limit communication between resources.
- Deny by default.
- Restrict inbound internet access and limit outbound access where appropriate.
- Implement secure connectivity to on-premises networks.

#### Compute
At this layer, it's important to:

- Secure access to virtual machines.
- Implement endpoint protection on devices and keep systems patched and current.

#### Application
Helps reduce the number of vulnerabilities introduced in code.
Every development team should ensure that its applications are secure by default.

At this layer, it's important to:

- Ensure that applications are secure + vulnerability free.
- Store sensitive application secrets in a secure storage medium.
- Make security a design requirement for all application development.

#### Data
Those who store and control access to data are responsible for ensuring that it's properly secured.

Often, regulatory requirements dictate controls and processes that must be in place to ensure:
- Confidentiality
- Integrity
- Availability of the data

In almost all cases, attackers are after data:

- Stored in a database.
- Stored on disk inside virtual machines.
- Stored in software as a service (SaaS) applications, such as Office 365.
- Managed through cloud storage.

### Describe the purpose of Microsoft Defender for Cloud 
A monitoring tool for security posture management + advanced threat protection.

Environments it monitors:
- Cloud
- On-premises
- Hybrid
- Multicloud

Provides:
- Guidance aimed at strengthening your security posture.
- Tools to:
    - Harden resources
    - Track your security posture
    - Cyber attacks protection
    - Provide streamlined security management

Helps you detect threats across:
- Azure PaaS services – Detect threats for:
    - Azure App Service
    - Azure SQL
    - Azure Storage Account
    - etc.
    Anomaly detection can be performed on Azure activity logs via Microsoft Defender for Cloud Apps.
- Azure data services – Can:
    - Classify data in Azure SQL
    - Create assessments for potential vulnerabilities across Azure SQL and Storage services
    - Recommend how to mitigate them
- Networks – Limits exposure to brute force attacks.
    - Reduce access to virtual machine ports. This prevents unwanted access.
    - Using the just-in-time VM access:
    > Secure temporary access policies on selected ports, only for authorized users with allowed source IP ranges/IPs

Automatically monitors and protects Azure services without additional deployment.

On-premises/other cloud environments are not automatically protected. To monitor them, you need:
- Log Analytics agent: Collects security and telemetry data.
- Azure Arc: Extends Defender for Cloud’s protection to non-Azure machines.
(Cloud security posture management (CSPM) features are extended to multicloud machines without needing agents)

For example, if you've connected an Amazon Web Services (AWS) account to an Azure subscription:

- Defender for Cloud's __CSPM features__ extend to your AWS resources.
    - This is an agentless plan
    - Assesses AWS resources'...
        - ...security according to AWS-specific security recommendations + includes the results in the secure score
        - ...compliance with built-in standards specific to AWS (AWS CIS, AWS PCI DSS, and AWS Foundational Security Best Practices).
    - The asset inventory page allows management of AWS resources alongside Azure resources
- __Microsoft Defender for Containers__ extends container threat detection + defenses to Amazon EKS Linux clusters.
- __Microsoft Defender for Servers__ brings threat detection + defenses to your Windows and Linux EC2 instances.

#### Asses, Secure, Defend
- Continuously assess
    - Aim:
        - Know your security posture
        - Identify and track vulnerabilities
    - Defender for Cloud provides vulnerability assessments for virtual machines, container registries, and SQL servers.
    - __Microsoft Defender for servers__ includes automatic, native integration with __Microsoft Defender for Endpoint__.
    - These assessment tools provide regular, detailed vulnerability scans covering:
        - Compute
        - Data
        - Infrastructure
    - They can be found in the Microsoft Defender Vulnerability Management Dashboard
- Secure
    - Aim:
    > Harden resources and services with Azure Security Benchmark
    - You must ensure workloads are secure for cloud security.
    - To do this, security policies tailored to your environment and situation must be in place.
    - Policies can run:
        - On management groups
        - Across subscriptions
        - For a whole tenant
    - Defender for Cloud is constantly monitoring for newly deployed resources and assesses if they're configured according to security best practices. If not, they're flagged and a prioritized list of recommendations for what needs to be fixed is provided.
    - Azure Security Benchmark is a set of guidelines for security and compliance best practices 
        - Based on common compliance frameworks 
        - Microsoft-authored, Azure-specific 

__Microsoft Defender for Cloud Secure Score Diagram:__

![Microsoft Defender for Cloud Secure Score Diagram][microsoft-defender-for-cloud-secure-score-diagram]

[microsoft-defender-for-cloud-secure-score-diagram]: https://github.com/Marko-Obradovic/azure-notes/blob/main/images/microsoft-defender-for-cloud-secure-score-diagram.png

- Defend
    - Aim:
    > Detect and resolve threats to resources, workloads, and services.
    - When Defender for Cloud detects a threat in any area of your environment, it generates a security alert. Security alerts:
        - Describe details of the affected resources
        - Suggest remediation steps
        - Provide, in some cases, an option to trigger a logic app in response
    - Defender for Cloud includes fusion kill-chain analysis.
        - Correlates alerts in your environment based on cyber kill-chain analysis.
        - Helps understand the full story of an attack campaign, where it started, and impact on resources.

Defender for cloud provides advanced threat protection features for many of your deployed resources, including:
- Virtual Machines
- SQL databases
- Containers
- Web applications
- Your network

Example Protection:
- Securing the management ports of your VMs with just-in-time access- Adaptive application controls to create allowlists for what apps should and shouldn't run on your machines.

# Describe Azure management and governance (30–35%) 
## Describe cost management in Azure 
### Describe factors that can affect costs in Azure 
Factors that impact OpEx cost:
- Resources:
    - Resource type
    - Resource settings
    - Azure region
> When you provision an Azure resource, Azure creates metered instances for that resource. The meters track the resources' usage and generate a usage record that is used to calculate your bill.

Example:
With a storage account, you specify a type such as blob, a performance tier, an access tier, redundancy settings, and a region. Creating the same storage account in different regions may show different costs and changing any of the settings may also impact the price.

Screenshot of storage blob settings showing hot and cool access tiers.

![Blob Storage][blob-storage]

[blob-storage]: https://github.com/Marko-Obradovic/azure-notes/blob/main/images/blob-storage.png

With a virtual machine (VM), you may have to consider licensing for the operating system or other software, the processor and number of cores for the VM, the attached storage, and the network interface. Just like with storage, provisioning the same virtual machine in different regions may result in different costs.


Screenshot of Azure virtual machine settings showing the virtual machine size options.

- Consumption
- Maintenance
- Geography
- Subscription type
- Azure Marketplace




Consumption
Pay-as-you-go has been a consistent theme throughout, and that’s the cloud payment model where you pay for the resources that you use during a billing cycle. If you use more compute this cycle, you pay more. If you use less in the current cycle, you pay less. It’s a straight forward pricing mechanism that allows for maximum flexibility.

However, Azure also offers the ability to commit to using a set amount of cloud resources in advance and receiving discounts on those “reserved” resources. Many services, including databases, compute, and storage all provide the option to commit to a level of use and receive a discount, in some cases up to 72 percent.

When you reserve capacity, you’re committing to using and paying for a certain amount of Azure resources during a given period (typically one or three years). With the back-up of pay-as-you-go, if you see a sudden surge in demand that eclipses what you’ve pre-reserved, you just pay for the additional resources in excess of your reservation. This model allows you to recognize significant savings on reliable, consistent workloads while also having the flexibility to rapidly increase your cloud footprint as the need arises.

Maintenance
The flexibility of the cloud makes it possible to rapidly adjust resources based on demand. Using resource groups can help keep all of your resources organized. In order to control costs, it’s important to maintain your cloud environment. For example, every time you provision a VM, additional resources such as storage and networking are also provisioned. If you deprovision the VM, those additional resources may not deprovision at the same time, either intentionally or unintentionally. By keeping an eye on your resources and making sure you’re not keeping around resources that are no longer needed, you can help control cloud costs.

Geography
When you provision most resources in Azure, you need to define a region where the resource deploys. Azure infrastructure is distributed globally, which enables you to deploy your services centrally or closest to your customers, or something in between. With this global deployment comes global pricing differences. The cost of power, labor, taxes, and fees vary depending on the location. Due to these variations, Azure resources can differ in costs to deploy depending on the region.

Network traffic is also impacted based on geography. For example, it’s less expensive to move information within Europe than to move information from Europe to Asia or South America.

Network Traffic
Billing zones are a factor in determining the cost of some Azure services.

Bandwidth refers to data moving in and out of Azure datacenters. Some inbound data transfers (data going into Azure datacenters) are free. For outbound data transfers (data leaving Azure datacenters), data transfer pricing is based on zones.

A zone is a geographical grouping of Azure regions for billing purposes. The bandwidth pricing page has additional information on pricing for data ingress, egress, and transfer.

Subscription type
Some Azure subscription types also include usage allowances, which affect costs.

For example, an Azure free trial subscription provides access to a number of Azure products that are free for 12 months. It also includes credit to spend within your first 30 days of sign-up. You'll get access to more than 25 products that are always free (based on resource and region availability).

Azure Marketplace
Azure Marketplace lets you purchase Azure-based solutions and services from third-party vendors. This could be a server with software preinstalled and configured, or managed network firewall appliances, or connectors to third-party backup services. When you purchase products through Azure Marketplace, you may pay for not only the Azure services that you’re using, but also the services or expertise of the third-party vendor. Billing structures are set by the vendor.

All solutions available in Azure Marketplace are certified and compliant with Azure policies and standards. The certification policies may vary based on the service or solution type and Azure service involved. Commercial marketplace certification policies has additional information on Azure Marketplace certifications.

### Compare the pricing calculator and the Total Cost of Ownership (TCO) Calculator 
### Describe cost management capabilities in Azure 
### Describe the purpose of tags 

## Describe features and tools in Azure for governance and compliance 
### Describe the purpose of Microsoft Purview in Azure 
### Describe the purpose of Azure Policy 
### Describe the purpose of resource locks 

## Describe features and tools for managing and deploying Azure resources 
### Describe the Azure portal 
### Describe Azure Cloud Shell, including Azure Command-Line Interface (CLI) and Azure PowerShell 
### Describe the purpose of Azure Arc 
### Describe infrastructure as code (IaC) 
### Describe Azure Resource Manager (ARM) and ARM templates 

## Describe monitoring tools in Azure 
### Describe the purpose of Azure Advisor 
### Describe Azure Service Health 
### Describe Azure Monitor, including Log Analytics, Azure Monitor alerts, and Application Insights 

