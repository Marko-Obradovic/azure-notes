# Describe cloud concepts (25–30%) 

## Describe cloud computing 
Define cloud computing 
======================
A service that provides computational resources over the internet.

Describe the shared responsibility model 
========================================
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
            IaaS: Customer
            PaaS: Shared
            SaaS: Shared
    - Applications
            IaaS: Customer
            PaaS: Shared
            SaaS: Cloud Provider
    - Network Controls
            IaaS: Customer
            PaaS: Shared
            SaaS: Cloud Provider
    - Operating Systems
            IaaS: Customer
            PaaS: Cloud Provider
            SaaS: Cloud Provider

Define each cloud model and outline their pros, cons and use cases  
==================================================================
1. Public:
    Definition:
        - A third-party service providing online computational resources
        - Physical infrastructure shared between organizations (multi-tenant environment)
        - Data and workloads are securely separated between organizations
    Pros:
        - No upfront payment
        - Quick and easy provisioning/deprovisioning of resources
        - Only pay for what you use
    Cons:
        - Less control over resources and security

2. Private:
    Definition:
        - A cloud solution dedicating all infrastructure to a single organization (single-tenant environment)
        - It can be on-prem, or provided by a third-party
    Pros:
        - Complete control over resources and security
        - Data is not collocated with others' data
    Cons:
        - Hardware must be purchased
        - You are responsible for hardware maintenance and updates

3. Hybrid:
    Definition: 
        - A computing environment that uses both public and private clouds in an inter-connected environment.
    Use case:
        - Can be used to allow a private cloud to scale for increased, temporary demand by deploying public cloud resources.
        - Can be used for an extra layer of security.
            E.g. Keeping some services on public cloud and others on private cloud infrastructure.
    Extra:
        - Most flexible option
        - You get to pick where your application is run
        - Organizations control security, compliance, or legal requirements

4. Multi-Cloud (New):
    Definition:
        - An environment where you deal with 2 or more public cloud providers and manage resources and security in both environments.

Describe the consumption-based model
====================================
CapEx (Capital Expenditure):
    One-time, up-front expenditure or purchase or secure tangible resources.
    e.g:
    - A new building
    - Repaving the parking lot
    - Building a datacenter

OpEx (Operational Expenditure):
    Spending money on services or products over time.
    e.g:
    - Renting a convention center
    - Leasing a company vehicle
    - Signing up for cloud services

Cloud computing falls under OpEx.
With Cloud Computing, you don't pay for physical infrastructure, electricity, security, or anything associated with maintaining a datacenter.
Instead, you ONLY pay for the IT resources and stop when you don't use them.

Benefits:
    - No upfront cost
    - No wasted resources
    - Pay for what you need
    - Stop paying when you don't

Compare cloud pricing models 
============================
(https://spot.io/resources/azure-pricing/the-complete-guide/) 
1. Pay as you go

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

2. Reserved Instances

You can purchase Reserved Virtual Machine Instances (RVMI's) for 1 or 3 years in a specific region
    - Can cancel, but there is an early termination fee
    - Can replace reserved instances during commitment period
    
Benefits:
    - Save up to 72% compared to Pay as you go.

Suitable for:
    - Apps with stable ongoing use
    - Organizations with a fixed budget
    - Large Scale applications where a certain amount of virtual machines are always in use

3. Spot Instances

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

Describe serverless 
====================
Definition: A provided infrastructure and runtime environment to deploy applications rapidly.
You don't need to worry about the:
    - Infrastructure
    - Scaling ─────────┐
    - Provisioning ────├───[of VMs]
    - Management ──────┘

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
https://learn.microsoft.com/en-us/training/modules/describe-benefits-use-cloud-services/ 

High availability: 
===================
Definition: Ensuring your app is available regardless of disruptions

Benefits: The higher your app's availability, the more time you save end-users in down-time. They can accomplish more.

Cons: The higher the service's availability, the more it will cost to run and keep at a high availability. This will then be more expensive for the end user.

Extra: When you're architecturing an app, you need to account for service availability guarantees (part of SLAs)

Scalability:
============
Definition: The ability to adjust resources to meet demand.

Benefits:
    - If you experience high traffic, you can add resources to handle it.
    - If demand drops, you can use less resources and pay less.

Reliability
===========
The ability of a system to recover from failure and continue to function.
The cloud allows you to have reliable and resilient infrastructure because it gives you access to deploy resources all around the world.

Benefit: If one region has a catastrophic event, the other regions are available to use.

Predictability 
===============
Performance Predictability: 
    Because of things like 
        - Auto scaling
        - Load balancing
        - High availability
    You can predicting the resources needed to deliver a positive experience for your customers.

Cost Predictability:
    You can use:
        - Total Cost of Ownership (TCO)
        - Pricing calculator to predict cost potential
    You can track resource usage in real time and monitor resources to make sure they're being used efficiently.

Security
========
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

Governance 
===========
governance ensures your cloud resources stay compliant, consistent, and under control

In practice, this means:
    - ARM templates/policies make sure resources are deployed with the right config.

    - Compliance & Audit tools scan your environment for resources that don’t meet standards:
        - Azure Policy
        - Blueprints

    - Automatic Updates to Standards across the whole cloud environment.

    - Centralized Management over who can deploy what, where, and how.

Describe the benefits of manageability in the cloud 
====================================================
Manageability: How you manage your cloud resources.
In practice:
    - Automatic resource scaling
    - Deploy from templates
    - Health monitoring
    - Alerts

## Describe cloud service types 
https://www.bigcommerce.co.uk/articles/ecommerce/saas-vs-paas-vs-iaas/
Define and outline the examples, use cases and responsibilities of:
===================================================================
☁️ 1. Infrastructure as a Service (IaaS)
Definition: IaaS provides virtualized computing resources over the internet, such as servers, storage, and networking, allowing users to run applications without buying physical hardware.

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

🧱 2. Platform as a Service (PaaS)
Definition: PaaS lets you build, deploy, and manage applications without managing infrastructure like servers or storage.

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

🌐 3. Software as a Service (SaaS)
Definition: SaaS platforms deliver software applications over the internet, managed by a third-party provider.

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
Describe Azure regions
======================
https://idodata.com/2025/05/06/az-900-describe-azure-regions-region-pairs-and-sovereign-regions/
A specific geographic area that contains one or more data centers.

Each region offers redundancy, scalability, and availability for Azure services.

Advantage:
    - Regions help businesses meet data residency requirements, such as regulations requiring data to remain within a specific geographic boundary (e.g., Europe).


Region Pairs,
=============
Azure pairs each region with another region in the same geography, typically at least 300 miles apart. This strategy is known as a region pair.

Benefits:
    - Region pairs are designed to enhance high availability and disaster recovery:
    - If one region fails or is affected by an outage, services can failover to the paired region.

Extra:
    - In the event of a geographic disaster affecting both regions, Azure prioritizes recovery for one of them.
    - Planned updates are intentionally not deployed simultaneously to both regions in a pair to reduce risk.

Sovereign regions
=================
Specially isolated Azure environments designed to meet strict national and governmental requirements.

1. United States Sovereign Regions
2. China Sovereign Regions
3. Germany Sovereign Region

Describe Azure datacenters
==========================
https://idodata.com/2025/05/08/az-900-describe-azure-datacenters/
An Azure datacenter is a physical building that contains large numbers of networked computer servers.

Each datacenter is located in a specific geographic location, chosen based on accessibility, climate stability, and regional demand.
Azure datacenters are designed to be self-sufficient, each with its own power supply, cooling systems, and network infrastructure.
Resources are not shared between datacenters, helping to reduce the risk of systemic failure.


Describe availability zones
===========================
https://learn.microsoft.com/en-us/azure/reliability/availability-zones-overview?tabs=azure-cli

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

Example Azure regions - regions 1 supports availability zones, region doesn't have availability zones.
├── Azure Region 1
│   ├── Availability Zone 1
│   │   └── Datacenter(s)
│   ├── Availability Zone 2
│   │   └── Datacenter(s)
│   └── Availability Zone 3
│       └── Datacenter(s)
└── Azure Region 2
    └── Datacenter(s)


Resources:
==========
An Azure resource is any manageable item available through Azure.

Examples:
    - Virtual Machines (VMs)
    - Storage Accounts
    - Web Apps
    - Databases
    - Virtual Networks

Resources are created, deployed, and managed using tools like the Azure Portal, CLI, PowerShell, or ARM templates.
Each resource has properties like location, type, and pricing tier.

Azure Solution:
===============
A conceptual bundle of services and resources designed to solve a specific business or technical need.
Example: A web hosting solution might include App Service, SQL Database, Key Vault, and CDN.

Resource Groups:
================
A container that holds related Azure resources for a solution.
Example: You might place all the resources from your web hosting solution into one resource group.

The resource group can include all the resources for the solution or only resources that you want to manage as a group.
You decide how to allocate resources to resource groups based on what makes the most sense for your organization.

Generally, resources sharing the same lifecycle share a resource group so it's easier to deploy, update, and delete them as a group.

The Azure portal uses the resource group scope to create views that span across multiple resources. For example:
- Metrics blade                 ->  Metrics info like CPU/resources.
- Deployments blade             ->  ARM template/Bicep deployment history of that resource group (includes portal deployments).
- Policy blade                  ->  Info related to policies enforced on the resource group.
- Diagnostics settings blade    ->  Errors/warnings to review.

The resource group stores metadata about the resources.
Specifying a location for the resource group dictates where that metadata is stored.
For compliance reasons, you might need to ensure that your data is stored in a particular region.
Resources inside a resource group can be in different regions.

Describe management groups
==========================

Describe subscriptions
======================
https://www.alifconsulting.com/post/azure-subscription

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

Azure Governance Hierarchy
==========================
└── Business Unit
    └── Geography (e.g., England)
        ├── Environment (e.g., Production)
        │   └── Management Group
        │       ├── Subscription A  ← [Access Control Boundary + Billing Boundary can be added]
        │       │   ├── Resource Group 1
        │       │   │   ├── Resource: Virtual Machine
        │       │   │   ├── Resource: Storage Account
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
-

## Describe Azure storage services 
Compare Azure Storage services 
===============================
https://learn.microsoft.com/en-us/azure/architecture/guide/technology-choices/storage-options

Azure Storage is a managed service for providing cloud storage.
Storage in Azure is highly available, secure, durable, scalable, and redundant.

🧱 Core Storage Services
These are the foundational storage types in Azure:
Azure Blob Storage
------------------
An object storage solution for the cloud.  
Optimized for storing massive amounts of unstructured data.

Use Cases:
    - Serving images or documents directly to a browser.
    - Storing files for distributed access.
    - Streaming video and audio.
    - Writing to log files.
    - Storing data for backup and restore, disaster recovery, and archiving.
    - Storing data for analysis by an on-premises or Azure-hosted service.


Azure Files
-----------
Azure Files provides fully managed, native SMB (Server Message Block) and NFS (Network File System) file shares, without the need to run a virtual machine.
You can mount an Azure file share as a network drive to any Azure virtual machine or on-premises computer.

Azure disk storage
------------------
    Azure disk storage offers persistent, high-performance block storage to power Azure Virtual Machines.
    Offer the industry's only single-instance, service-level agreement (SLA) for virtual machines that use Azure Premium SSD or Azure Ultra Disk Storage.
    Azure manages disks as a top-level resource.

    Properties of Azure Disks:
        - Highly durable
        - Secure
        - high availability
            > Provides availability sets and availability zones for your Azure Virtual Machines fault domains.

    Azure Resource Manager (ARM) capabilities are provided by default, including:
        - Azure Role-Based Access Control (RBAC): Assigns fine-grained permissions to users, groups, and applications for managing resources securely.
        - Policies: Enforces rules and compliance standards across your Azure environment.
        - Tagging: Adds metadata labels to resources for better organization, cost tracking, and automation.

Data Lake Storage Gen2
----------------------
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


🔄 **Integration & Sync Tools**
These services extend or connect core storage:

Azure File Sync
---------------
For centralizing file shares in Azure Files.
Azure File Sync offers the flexibility, performance, and compatibility of an on-premises file server.

Works With:
    - Azure Files

Azure Data Box
--------------
A solution that allows for offline, bulk data transfer in and out of Azure using a physical storage appliance.
It's used when network-based data transfer is constrained by:
    - Time
    - Network availability
    - Cost

Works With:
    - Blob
    - Files
    - Disks

Data Box Gateway
----------------
A storage solution that enables you to seamlessly send data to Azure.
It's a virtual device based on a virtual machine provisioned in your virtualized environment/hypervisor.
The virtual device is on-premises and you write data to it by using the NFS and SMB protocols.
The device then transfers your data to:
    - Azure block blobs
    - Page blobs
    - Azure Files.

🧰 **Advanced & Specialized Storage**
These are optimized for performance, container workloads, or HPC (High-Performance Computing):

Azure NetApp Files
------------------
A file storage service that's:
    - enterprise-class
    - high-performance

Supports any workload type and is highly available by default.
You can select service and performance levels and set up snapshots through the service.

Use Cases:
    - SAP
    - Oracle
    - HPC

Azure Managed Lustre
--------------------
A high-performance distributed parallel file system solution.
ideal for HPC workloads that require high throughput and low latency.
Use Cases:
    - AI/ML
    - genomics

Azure Container Storage
-----------------------
A volume management + deployment + orchestration service that is:
    - Fully managed
    - Cloud-based
    - Built natively for containers.
    
It integrates with Kubernetes
    - Allows you to dynamically + automatically provision persistent volumes to store data for stateful applications running on Kubernetes clusters.

🧳 Edge & Hybrid Solutions
These bring Azure Storage closer to your location:

Azure Stack Edge
----------------
An on-prem network device that moves data into and out of Azure.
Has AI-enabled edge compute to pre-process data during upload.

(Data Box Gateway is a virtual version of the device but with the same data transfer capabilities)

Use Cases:
    - Local inference
    - data preprocessing



Describe storage tiers 
=======================
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

Describe redundancy options 
============================
Describe storage account options and storage types 
===================================================
Identify options for moving files, including AzCopy, Azure Storage Explorer, and Azure File Sync 
=================================================================================================
Describe migration options, including Azure Migrate and Azure Data Box 
=======================================================================

## Describe Azure identity, access, and security 
Describe directory services in Azure, including Microsoft Entra ID and Microsoft Entra Domain Services 
=======================================================================================================
Describe authentication methods in Azure, including single sign-on (SSO), multi-factor authentication (MFA), and passwordless 
==============================================================================================================================
Describe external identities in Azure, including business-to-business (B2B) and business-to-customer (B2C) 
===========================================================================================================
Describe Microsoft Entra Conditional Access 
============================================
Describe Azure role-based access control (RBAC) 
================================================
Describe the concept of Zero Trust 
===================================
Describe the purpose of the defense-in-depth model 
===================================================
Describe the purpose of Microsoft Defender for Cloud 
=====================================================

# Describe Azure management and governance (30–35%) 
## Describe cost management in Azure 
Describe factors that can affect costs in Azure 
================================================
Compare the pricing calculator and the Total Cost of Ownership (TCO) Calculator 
================================================================================
Describe cost management capabilities in Azure 
===============================================
Describe the purpose of tags 
=============================

## Describe features and tools in Azure for governance and compliance 
Describe the purpose of Microsoft Purview in Azure 
===================================================
Describe the purpose of Azure Policy 
=====================================
Describe the purpose of resource locks 
=======================================

## Describe features and tools for managing and deploying Azure resources 
Describe the Azure portal 
==========================
Describe Azure Cloud Shell, including Azure Command-Line Interface (CLI) and Azure PowerShell 
==============================================================================================
Describe the purpose of Azure Arc 
==================================
Describe infrastructure as code (IaC) 
======================================
Describe Azure Resource Manager (ARM) and ARM templates 
========================================================

## Describe monitoring tools in Azure 
Describe the purpose of Azure Advisor 
======================================
Describe Azure Service Health 
==============================
Describe Azure Monitor, including Log Analytics, Azure Monitor alerts, and Application Insights 
================================================================================================

