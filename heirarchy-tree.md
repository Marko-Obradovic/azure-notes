```
AZURE HIERARCHY OVERVIEW
========================

1. GLOBAL INFRASTRUCTURE
   ├─ Azure Regions
   │   ├─ Azure Datacenters
   │   ├─ Availability Zones
   │   │   ├─ Fault Domains
   │   │   └─ Update Domains
   │   ├─ Region Pairs
   │   └─ Sovereign Regions
   └─ Azure Virtual Networks (VNet)
       ├─ Azure Subnets
       ├─ VNet Peering
       ├─ Azure DNS
       ├─ Azure VPN Gateway
       ├─ Azure ExpressRoute
       ├─ Public Endpoints
       └─ Private Endpoints

2. RESOURCE ORGANIZATION & GOVERNANCE
   ├─ Management Groups
   │   └─ Contain Subscriptions
   ├─ Subscriptions
   │   ├─ Billing Boundary
   │   └─ Access Control Boundary
   ├─ Resource Groups
   │   ├─ Contain Resources
   │   ├─ Tags
   │   ├─ Resource Locks
   │   ├─ Azure Policy / Policy Initiatives
   │   ├─ Blueprints
   │   ├─ Governance & Compliance Tools
   │   │   ├─ Azure Policy
   │   │   ├─ Microsoft Purview
   │   │   └─ Azure Blueprints
   │   ├─ Blades
   │   │   ├─ Metrics blade
   │   │   ├─ Deployments blade
   │   │   ├─ Policy blade
   │   │   └─ Diagnostics settings blade
   │   └─ Azure Solution (logical grouping of related resources)
   └─ Azure Resource Manager (ARM)
       ├─ Manages all deployments & resources
       ├─ ARM Templates / Bicep (Infrastructure as Code)
       └─ Azure Resource Manager Benefits

3. BILLING & COST MANAGEMENT
   ├─ Pricing Models
   │   ├─ Pay-As-You-Go
   │   ├─ Reserved Instances
   │   └─ Spot Instances
   ├─ Azure Marketplace
   ├─ Pricing Calculator
   └─ Cost Management Tool

4. COMPUTE SERVICES
   ├─ Virtual Machines (VMs)
   │   ├─ Resources required for virtual machines
   │   ├─ Virtual Machine Scale Sets
   │   ├─ Virtual Machine Availability Sets
   │   │   ├─ Update Domains
   │   │   └─ Fault Domains
   │   ├─ Lift and Shift (migration approach)
   │   └─ Azure Virtual Desktop
   ├─ Containers
   │   ├─ Azure Container Instances
   │   ├─ Azure Container Apps
   │   └─ Azure Kubernetes Service (AKS)
   ├─ Functions (Serverless Compute)
   ├─ Web Apps (Azure App Service)
   ├─ HPC (High Performance Computing)
   └─ Azure Stack Edge (hybrid compute)

5. STORAGE SERVICES
   ├─ Storage Accounts
   │   ├─ Storage Types
   │   │   ├─ Standard general-purpose v2
   │   │   ├─ Premium block blobs
   │   │   ├─ Premium file shares
   │   │   └─ Premium page blobs
   │   ├─ Storage Tiers
   │   │   ├─ Hot tier
   │   │   ├─ Cool tier
   │   │   ├─ Cold tier
   │   │   └─ Archive tier
   │   ├─ Redundancy Options
   │   │   ├─ LRS  - Locally Redundant Storage
   │   │   ├─ ZRS  - Zone Redundant Storage
   │   │   ├─ GRS  - Geo Redundant Storage
   │   │   ├─ RA-GRS
   │   │   ├─ GZRS
   │   │   └─ RA-GZRS
   │   └─ Tools
   │       ├─ AzCopy
   │       └─ Azure Storage Explorer
   ├─ Azure Blob Storage
   ├─ Azure Files
   ├─ Azure Disk Storage
   ├─ Azure Data Lake Storage Gen2
   ├─ Azure File Sync
   ├─ Azure Data Box / Data Box Gateway
   ├─ Azure NetApp Files
   ├─ Azure Managed Lustre
   └─ Azure Container Storage

6. IDENTITY & ACCESS MANAGEMENT (Microsoft Entra)
   ├─ Microsoft Entra ID (formerly Azure AD)
   │   ├─ Authentication Methods
   │   │   ├─ Kerberos / NTLM
   │   │   ├─ LDAP
   │   │   ├─ Passwordless authentication
   │   │   ├─ FIDO2 security keys
   │   │   ├─ Microsoft Entra Multifactor Authentication (MFA)
   │   │   └─ Single Sign-On (SSO)
   │   ├─ Connect Sync (Microsoft Entra Connect)
   │   ├─ Microsoft Entra Domain Services
   │   │   ├─ Domain Join
   │   │   └─ Group Policy
   │   ├─ External Identity
   │   │   ├─ Microsoft Entra External ID
   │   │   ├─ B2B Collaboration
   │   │   ├─ B2B Direct Connect
   │   │   └─ Azure AD B2C
   │   ├─ Conditional Access
   │   │   ├─ Conditional Access (concept)
   │   │   └─ Microsoft Entra Conditional Access
   │   └─ Azure Role-Based Access Control (RBAC)
   ├─ Zero Trust (security model)
   └─ Defense-in-Depth Model
       ├─ Physical Security Layer
       ├─ Identity & Access Layer
       ├─ Perimeter Layer
       ├─ Network Layer
       ├─ Compute Layer
       ├─ Application Layer
       └─ Data Layer

7. SECURITY & PROTECTION SERVICES
   ├─ Azure Firewall
   ├─ Azure Load Balancer
   ├─ Microsoft Defender for Cloud
   │   ├─ CSPM Features (Cloud Security Posture Management)
   │   ├─ Microsoft Defender for Containers
   │   ├─ Microsoft Defender for Servers
   │   ├─ Assess
   │   ├─ Secure
   │   └─ Defend
   ├─ Microsoft Defender Family (part of Zero Trust)
   └─ Azure Policy / Compliance Integration

8. MONITORING, HEALTH & OPTIMIZATION
   ├─ Azure Monitor
   │   ├─ Azure Log Analytics
   │   ├─ Azure Monitor Alerts
   │   └─ Application Insights
   ├─ Azure Service Health
   ├─ Azure Advisor (cost, reliability, security, performance)
   ├─ Azure Migrate
   └─ Azure Arc (manage hybrid & multi-cloud)

9. TOOLS & INTERFACES
   ├─ Azure Portal (web UI)
   ├─ Azure REST API
   ├─ Azure PowerShell
   ├─ Azure Command-Line Interface (CLI)
   ├─ Azure Cloud Shell
   ├─ Infrastructure as Code (IaC)
   │   ├─ ARM Templates
   │   ├─ Bicep
   │   └─ Terraform (3rd-party)
   └─ Service Types
       ├─ Infrastructure as a Service (IaaS)
       ├─ Platform as a Service (PaaS)
       └─ Software as a Service (SaaS)

10. SERVICE-LEVEL AGREEMENTS (SLA)
    └─ Define availability and performance guarantees per Azure service

```
