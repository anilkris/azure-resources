# Exam AZ-303: Microsoft Azure Architect Technologies 

## Implement and Monitor an Azure Infrastructure (50-55%)

### Implement cloud infrastructure monitoring

*  monitor security

*  monitor performance

    * configure diagnostic settings on resources

    *  create a performance baseline for resources

    *  monitor for unused resources

    *  monitor performance capacity

    *  visualize diagnostics data using Azure Monitor

* monitor health and availability

  *  monitor networking
  *  monitor service health

* monitor cost

  * monitor spend 
  * report on spend

* configure advanced logging

  * implement and configure Azure Monitor insights, including App Insights, Networks,
    Containers

  * configure a Log Analytics workspace

* configure logging for workloads

  * initiate automated responses by using Action Groups

* configure and manage advanced alerts

  * collect alerts and metrics across multiple subscriptions 
  * view Alerts in Azure Monitor logs
  
  *  NOT: create Log Analytics query

###  Implement storage accounts
* select storage account options based on a use case

* configure Azure Files and blob storage

* configure network access to the storage account
* implement Shared Access Signatures and access policies
* implement Azure AD authentication for storage
* manage access keys
* implement Azure storage replication
  * implement Azure storage account failover

### Implement VMs for Windows and Linux

* configure High Availability

* configure storage for VMs

* select virtual machine size

* implement Azure Dedicated Hosts

* deploy and configure scale sets

* configure Azure Disk Encryption

[DiskEncryption](https://github.com/anilkris/azure-resources/blob/master/EcnryptVM.md , DiskEncryptionPowershell)

### Automate deployment and configuration of resources

* save a deployment as an Azure Resource Manager template
* modify Azure Resource Manager template
* evaluate location of new resources
* configure a virtual disk template
* deploy from a template
* manage a template library
* create and execute an automation runbook

### Implement virtual networking

* implement VNet to VNet connections

* implement VNet peering


### Implement Azure Active Directory

* add custom domains

* configure Azure AD Identity Protection

* implement self-service password reset

* implement Conditional Access including MFA
 
 * configure user accounts for MFA

* configure fraud alerts

* configure bypass options

* configure Trusted IPs

* configure verification methods

* implement and manage guest accounts

* manage multiple directories

### Implement and manage hybrid identities

* install and configure Azure AD Connect

*  identity synchronization options

* configure and manage password sync and password writeback

* configure single sign-on

* use Azure AD Connect Health

## Implement Management and Security Solutions (25-30%)

#### Manage workloads in Azure

 * migrate workloads using Azure Migrate

   * assess infrastructure

   * select a migration method

   * prepare the on-premises for migration o recommend target infrastructure

* implement Azure Backup for VMs

* implement disaster recovery

* implement Azure Update Management

* Implement load balancing and network security

* implement Azure Load Balancer

* implement an application gateway

* implement a Web Application Firewall

* implement Azure Firewall

* implement the Azure Front Door Service

* implement Azure Traffic Manager

* implement Network Security Groups and Application Security Groups

* implement Bastion

### Implement and manage Azure governance solutions
 
* create and manage hierarchical structure that contains management groups,
 subscriptions and resource groups

* assign RBAC roles

* create a custom RBAC role

* configure access to Azure resources by assigning roles

* configure management access to Azure

* interpret effective permissions

* set up and perform an access review

* implement and configure an Azure Policy

* implement and configure an Azure Blueprint

###  Manage security for applications

* implement and configure KeyVault

* implement and configure Azure AD Managed Identities

* register and manage applications in Azure AD

## Implement Solutions for Apps (10-15%)
### Implement an application infrastructure

* create and configure Azure App Service

* create an App Service Web App for Containers

* create and configure an App Service plan

* configure an App Service

* configure networking for an App Service

* create and manage deployment slots

* implement Logic Apps

* implement Azure Functions

### Implement container-based applications

* create a container image

* configure Azure Kubernetes Service

* publish and automate image deployment to the Azure Container Registry

* publish a solution on an Azure Container Instance •

NOT: Service Fabric

## Implement and Manage Data Platforms (10-15%)
### Implement NoSQL databases

* configure storage account tables

* select appropriate CosmosDB APIs
 
* set up replicas in CosmosDB Implement Azure SQL databases

### Implement SQL databases

* configure Azure SQL database settings

* implement Azure SQL Database managed instances

* configure HA for an Azure SQL database

* publish an Azure SQL database