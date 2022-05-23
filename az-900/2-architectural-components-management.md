# Management

![Management Hierarchy](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/hierarchy-372fef74.png)

1. **Resources**: Resources are instances of services that you create, like virtual machines, storage, or SQL databases.
1. **Resource groups**: Resources are combined into resource groups, which act as a logical container into which Azure resources like web apps, databases, and storage accounts are deployed and managed.
1. **Subscriptions**: A subscription groups together user accounts and the resources that have been created by those user accounts. For each subscription, there are limits or quotas on the amount of resources that you can create and use. Organizations can use subscriptions to manage costs and the resources that are created by users, teams, or projects.
1. **Management groups**: These groups help you manage access, policy, and compliance for multiple subscriptions. All subscriptions 1. in a management group automatically inherit the conditions applied to the management group.

## Resource Groups

A resource group is a logical container for resources deployed on Azure.

### What?

-   All resources must be in a resource group, and a resource can only be a member of a single resource group.
-   Resource groups can't be nested.
-   Before any resource can be provisioned, you need a resource group for it to be placed in.
-   Many resources can be moved between resource groups with some services having specific limitations or requirements to move.
-   [Resource group limits](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/azure-subscription-service-limits#resource-group-limits)
-   You can group/organize multiple subscriptions into invoice sections.
    -   Each invoice section is a line item on the invoice that shows the charges incurred that month.
-   **Billing Profiles**
    -   Each billing profile has its **own monthly invoice and payment method**.
    -   You can set up multiple Billing Profiles in the same billing account.
        ![Billing structure](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/billing-structure-overview-2c81a8ad.png)

### Why?

-   **Logical grouping**: So you can provide order and organization to resources you create in Azure.
-   **Life cycle**: If you delete a resource group, all resources contained within it are also deleted
-   **Authorization**: Resource groups are also a scope for applying role-based access control (RBAC) permissions.

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

## Azure management groups

### What?

Azure management groups provide a way to efficiently manage access, policies, and compliance for all subscriptions of your organization.

-   Azure management groups provide a level of scope above subscriptions.
-   All subscriptions within a management group automatically inherit the conditions applied to the management group.
-   All subscriptions within a single management group must trust the same Azure AD tenant.
-   [Management Group limits](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/azure-subscription-service-limits#management-group-limits)

### Why?

-   You can have security policies that can't be altered by the resource or subscription owner, which allows for improved governance.
-   You can provide access to users to multiple subscriptions.
-   You can manage access and assign role-based access control to multiple subscriptions at once.

![Example](https://docs.microsoft.com/en-us/learn/azure-fundamentals/azure-architecture-fundamentals/media/management-groups-and-subscriptions-bba71896.png)

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
