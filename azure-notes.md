# Describe cloud concepts (25–30%) 

## Describe cloud computing 
Define cloud computing 
-
A service that provides computational resources over the internet.

Describe the shared responsibility model 
-
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

Define each cloud model and outline their pros, cons and use cases:  
-
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
-
>>> Context
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

>>>

Cloud computing falls under OpEx.
With Cloud Computing, you don't pay for physical infrastructure, electricity, security, or anything associated with maintaining a datacenter.
Instead, you ONLY pay for the IT resources and stop when you don't use them.

Benefits:
    - No upfront cost
    - No wasted resources
    - Pay for what you need
    - Stop paying when you don't

Compare cloud pricing models 
-
(https://spot.io/resources/azure-pricing/the-complete-guide/) 
1. Pay as you go

Pay for services on Azure according to actual usage
    - Billed per second
    - No long term commitment or upfront payment

• Benefits:
    - Flexibility to increase/decrease resources as needed
    - VMs can be scaled automatically
    
• Suitable for:
    - Users that prefer flexibility
    - Users that prefer to convert capital expenses into operating expenses
    - Users that Host applications with volatile/short term workloads

2. Reserved Instances

You can purchase Reserved Virtual Machine Instances (RVMI's) for 1 or 3 years in a specific region
    - Can cancel, but there is an early termination fee
    - Can replace reserved instances during commitment period
    
• Benefits:
    - Save up to 72% compared to Pay as you go.

• Suitable for:
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

• Suitable for:
    - 
    
Describe serverless 
-
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
-

High Scalability:
-

Reliability
-

Predictability 
-

Security
-
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
-
governance ensures your cloud resources stay compliant, consistent, and under control

In practice, this means:
    - ARM templates/policies make sure resources are deployed with the right config.

    - Compliance & Audit tools scan your environment for resources that don’t meet standards:
        - Azure Policy
        - Blueprints

    - Automatic Updates to Standards across the whole cloud environment.

    - Centralized Management over who can deploy what, where, and how.

Describe the benefits of manageability in the cloud 
-
Manageability: How you manage your cloud resources.
In practice:
    - Automatic resource scaling
    - Deploy from templates
    - Health monitoring
    - Alerts

## Describe cloud service types 
https://www.bigcommerce.co.uk/articles/ecommerce/saas-vs-paas-vs-iaas/
Define and outline the examples, use cases and responsibilities of:
-
    - IaaS 
        Definition: IaaS services provide virtualized computing resources over the internet
        Examples:
            - Azure Virtual Machines
            - Azure Virtual Network
            - Azure Load Balancer
        Use Cases:
        Your Responsibilities: (Reference table above)
        Provider's Responsibilities: (Reference table above)
        Shared Responsibilities: None
    - PaaS
        Definition: PaaS lets you build, deploy, and manage applications without managing infrastructure 
        Examples:
            - Azure Functions
            - Azure SQL Database
            - Azure Kubernetes Service (AKS)
        Use Cases:
        Your Responsibilities: (Reference table above)
        Provider's Responsibilities: (Reference table above)
        Shared Responsibilities: (Reference table above)
    - SaaS 
        Definition:
        Examples:
        Use Cases:
        Your Responsibilities: (Reference table above)
        Provider's Responsibilities: (Reference table above)
        Shared Responsibilities: (Reference table above)

# Describe Azure architecture and services (35–40%) 

## Describe the core architectural components of Azure
Describe Azure regions, region pairs, and sovereign regions
-
Describe availability zones
-
Describe Azure datacenters
-
Describe Azure resources and resource groups
-
Describe subscriptions
-
Describe management groups
-
Describe the hierarchy of resource groups, subscriptions, and management groups
-

## Describe Azure storage services 
Compare Azure Storage services 
-
Describe storage tiers 
-
Describe redundancy options 
-
Describe storage account options and storage types 
-
Identify options for moving files, including AzCopy, Azure Storage Explorer, and Azure File Sync 
-
Describe migration options, including Azure Migrate and Azure Data Box 
-

## Describe Azure identity, access, and security 
Describe directory services in Azure, including Microsoft Entra ID and Microsoft Entra Domain Services 
-
Describe authentication methods in Azure, including single sign-on (SSO), multi-factor authentication (MFA), and passwordless 
-
Describe external identities in Azure, including business-to-business (B2B) and business-to-customer (B2C) 
-
Describe Microsoft Entra Conditional Access 
-
Describe Azure role-based access control (RBAC) 
-
Describe the concept of Zero Trust 
-
Describe the purpose of the defense-in-depth model 
-
Describe the purpose of Microsoft Defender for Cloud 
-

# Describe Azure management and governance (30–35%) 
## Describe cost management in Azure 
Describe factors that can affect costs in Azure 
-
Compare the pricing calculator and the Total Cost of Ownership (TCO) Calculator 
-
Describe cost management capabilities in Azure 
-
Describe the purpose of tags 
-

## Describe features and tools in Azure for governance and compliance 
Describe the purpose of Microsoft Purview in Azure 
-
Describe the purpose of Azure Policy 
-
Describe the purpose of resource locks 
-

## Describe features and tools for managing and deploying Azure resources 
Describe the Azure portal 
-
Describe Azure Cloud Shell, including Azure Command-Line Interface (CLI) and Azure PowerShell 
-
Describe the purpose of Azure Arc 
-
Describe infrastructure as code (IaC) 
-
Describe Azure Resource Manager (ARM) and ARM templates 
-

## Describe monitoring tools in Azure 
Describe the purpose of Azure Advisor 
-
Describe Azure Service Health 
-
Describe Azure Monitor, including Log Analytics, Azure Monitor alerts, and Application Insights 
-

