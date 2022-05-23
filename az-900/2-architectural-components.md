# Management

![Management Hierarchy](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/hierarchy-372fef74.png)

1. **Resources**: Resources are instances of services that you create, like virtual machines, storage, or SQL databases.
1. **Resource groups**: Resources are combined into resource groups, which act as a logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed.
1. **Subscriptions**: A subscription groups together user accounts and the resources that have been created by those user accounts. For each subscription, there are limits or quotas on the amount of resources that you can create and use. Organizations can use subscriptions to manage costs and the resources that are created by users, teams, or projects.
1. **Management groups**: These groups help you manage access, policy, and compliance for multiple subscriptions. All subscriptions 1. in a management group automatically inherit the conditions applied to the management group.

## Resource Groups

A resource group is a logical container for resources deployed on Azure.

1. What?
    - All resources must be in a resource group, and a resource can only be a member of a single resource group.
    - Resource groups can't be nested.
    - Before any resource can be provisioned, you need a resource group for it to be placed in.
    - Many resources can be moved between resource groups with some services having specific limitations or requirements to move.
    - [Resource group limits](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/azure-subscription-service-limits#resource-group-limits)
    - You can group/organize multiple subscriptions into invoice sections.
        - Each invoice section is a line item on the invoice that shows the charges incurred that month.
    - **Billing Profiles**
        - Each billing profile has its **own monthly invoice and payment method**.
        - You can set up multiple Billing Profiles in the same billing account.
          ![Billing structure](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/billing-structure-overview-2c81a8ad.png)
1. Why?
    - **Logical grouping**: So you can provide order and organization to resources you create in Azure.
    - **Life cycle**: If you delete a resource group, all resources contained within it are also deleted
    - **Authorization**: Resource groups are also a scope for applying role-based access control (RBAC) permissions.

## Azure Subscriptions

### What?

An Azure subscription is a logical unit of Azure services that links to an Azure account, which is an identity in Azure Active Directory (Azure AD) or in a directory that Azure AD trusts.

Important Notes:

-   Using Azure requires an Azure subscription.
-   An account can have one subscription or multiple subscriptions that have different billing models and to which you apply different access-management policies
-   Azure subscriptions can define boundaries around Azure products, services, and resources.
    -   **Billing boundary**: Azure generates separate billing reports and invoices for each subscription so that you can organize and manage costs.
    -   **Access control boundary**: This billing model allows you to manage and control access to the resources that users provision with specific subscriptions.
-   Azure subscriptions allow you to manage and control access to the resources that users provision within each subscription.
-   [**Subscription limits**](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/azure-subscription-service-limits#subscription-limits): Subscriptions are bound to some hard limitations. Those limits should be considered as you create subscriptions on your account. If there's a need to go over those limits in particular scenarios, you might need additional subscriptions.

#### Why?

-   **Environments**
    -   Different Access control at the subscription level for each environment (testing, development, production).
    -   Better Data **Isolation**.
    -   Better support for **compliance** requirements
-   **Organizational structures**
    -   You might want certain departments to not have access to some resources. For example, not all developers need access to virtual machines that have 300+ GB of RAM.
-   **Billing**
    -   Because costs are first aggregated at the subscription level, you might want to create subscriptions to manage and track costs based on your needs.

## Azure Resource Manager

![Azure Resource Manager](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/consistent-management-layer-feef9259.png)

#### What?

Azure Resource Manager is the deployment and management service for Azure.

#### Why?

-   It provides a management layer that enables you to create, update, and delete resources in your Azure account.
    -   Deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.
-   Acts as a Gateway for Azure tools, APIs, or SDKs.
-   It authenticates and authorizes the request.
    -   Apply access control to all services because RBAC is natively integrated into the management platform.
-   Because all requests are handled through the same API, you see consistent results and capabilities in all the different tools.
-   Manage your infrastructure through declarative templates rather than scripts. A Resource Manager template is a JSON file that defines what you want to deploy to Azure.
-   Ensures Consistency.
    -   Define the dependencies between resources so they're deployed in the correct order.

# Azure Regions

## What?

A **region** is a geographical area on the planet that contains at least one but potentially multiple datacenters that are nearby and networked together with a low-latency network. Azure intelligently assigns and controls the resources within each region to ensure workloads are appropriately balanced.

Worth Mentioning:

-   Some services or VM features are only available in certain regions.
-   Some global Azure services don't require you to select a particular region, such as **Azure Active Directory, Azure Traffic Manager, and Azure DNS**.

## Where?

![June 2020 Available Regions](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/regions-small-be724495.png)
You can check the map for the [infrastructure map](https://infrastructuremap.microsoft.com/explore) for the latest updates.

## Why?

1. Regions give you the flexibility to bring applications closer to your users no matter where they are. In other words they help you improve the **performance** of your application.
1. Global regions provide better **scalability and redundancy**.
1. They preserve **data residency** for your services.

## Special Azure Regions

Azure has specialized regions that you might want to use when you build out your applications for **compliance or legal purposes**.

A few examples:

-   US DoD Central, US Gov Virginia, US Gov Iowa and more: These regions are physical and logical network-isolated instances of Azure for U.S. government agencies and partners. These datacenters are operated by screened U.S. personnel and include additional compliance certifications.
-   China East, China North, and more: These regions are available through a unique partnership between Microsoft and 21Vianet, whereby Microsoft doesn't directly maintain the datacenters.

## Azure Pair Regions

Each Azure region is always paired with another region within the same geography at least 300 miles away.
![Region Pairs](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/region-pairs-d9eb9728.png)

Features:

-   If an extensive Azure outage occurs, one region out of every pair is prioritized to make sure at least one is restored as quickly as possible for applications hosted in that region pair.
-   Planned Azure updates are rolled out to paired regions one region at a time to minimize downtime and risk of application outage.
-   Data continues to reside within the same geography as its pair (except for Brazil South) for tax- and law-enforcement jurisdiction purposes.

# Azure availability zones

## What?

Availability zones are physically separate datacenters within an Azure region.

Features:

1. Each availability zone is made up of one or more datacenters equipped with independent power, cooling, and networking.
1. An availability zone is set up to be an isolation boundary.
1. Availability zones are connected through high-speed, private fiber-optic networks.
1. There's a **minimum of three zones** within a single region.

![Availability Zones](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/availability-zones-5c3c490c.png)

## Where?

Not every region has support for availability zones.You can find a list of [Azure regions with availability zones here.](https://docs.microsoft.com/en-us/azure/availability-zones/az-region#azure-regions-with-availability-zones)

## Why?

1. **Run mission-critical** applications and build **high-availability** into your application architecture by co-locating your compute, storage, networking, and data resources within a zone and **replicating** in other zones.

## Types of services

-   **Zonal services**: You pin the resource to a specific zone.
-   **Zone-redundant services**: The platform replicates automatically across zones.
-   **Non-regional services**: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.
