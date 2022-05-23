# Cloud Computing

## [What?](https://azure.microsoft.com/en-us/overview/what-is-cloud-computing/#benefits)

It's the delivery of computing services over the internet, which is otherwise known as the cloud.

## Why?

-   Lower your operating costs.
-   Run your infrastructure more efficiently.
-   Scale as your business needs change.

    -   **Scalability**: Apps in the cloud can scale vertically and horizontally:

        -   Scale vertically to increase compute capacity by adding RAM or CPUs to a virtual machine.
        -   Scaling horizontally increases compute capacity by adding instances of resources, such as adding VMs to the configuration.

    -   **Elasticity**: You can configure cloud-based apps to take advantage of autoscaling, so your apps always have the resources they need.

-   Teams deliver new features to their users at record speeds.
    -   **Agility**: Deploy and configure cloud-based resources quickly as your app requirements change.
-   Users expect an increasingly rich and immersive experience with their devices and with software.
-   **High availability**: Depending on the service-level agreement (SLA) that you choose, your cloud-based apps can provide a continuous user experience with no apparent downtime, even when things go wrong.
-   **Geo-distribution**: You can deploy apps and data to regional datacenters around the globe, thereby ensuring that your customers always have the best performance in their region.
-   **Disaster recovery**: By taking advantage of cloud-based backup services, data replication, and geo-distribution, you can deploy your apps with the confidence that comes from knowing that your data is safe in the event of a disaster.
-   You have access to:
    -   A nearly limitless pool of raw compute, storage, and networking components.
    -   Speech recognition and other cognitive services that help make your application stand out from the crowd.
    -   Analytics services that deliver telemetry data from your software and devices.

# Capital expenses vs. operating expenses

## Capital Expenditure (CapEx)

It is the up-front spending of money on physical infrastructure, and then deducting that up-front expense over time. The up-front cost from CapEx has a value that reduces over time.

## Operational Expenditure (OpEx)

OpEx is spending money on services or products now, and being billed for them now. You can deduct this expense in the same year you spend it. There is no up-front cost, as you pay for a service or product as you use it.

# Cloud service Models

![Service included in each Cloud Service Model](https://docs.microsoft.com/en-us/learn/azure-fundamentals/fundamental-azure-concepts/media/iaas-paas-saas-575a09e9.png)
![Responsibility in each Cloud Service Model](https://docs.microsoft.com/en-us/learn/azure-fundamentals/fundamental-azure-concepts/media/shared-responsibility-76efbc1e.png)

## IaaS - Infrastructure-as-a-Service

It aims to give you complete control over the hardware that runs your application. Instead of buying hardware, with IaaS, you rent it.

-   Advantages

    -   **No CapEx**. Users have no up-front costs.

    -   **Agility**. Applications can be made accessible quickly, and deprovisioned whenever needed.

    -   **Management**. The shared responsibility model applies; the user manages and maintains the services they have provisioned, and the cloud provider manages and maintains the cloud infrastructure.

    -   **Consumption-based model**. Organizations pay only for what they use and operate under an Operational Expenditure (OpEx) model.

    -   **Skills**. No hardware skills required.

    -   **Cloud benefits**. Organizations can use the skills and expertise of the cloud provider to ensure workloads are made secure and highly available.

    -   **Flexibility**. You have control to configure and manage the hardware running your application.

## PaaS - Platform-as-a-Service

In this cloud service model, the cloud provider manages the virtual machines and networking resources, and the cloud tenant deploys their applications into the managed hosting environment

-   Advantages

    -   **No CapEx**. Users have no up-front costs.

    -   **Agility**. PaaS is more agile than IaaS, and users don't need to configure servers for running applications.

    -   **Consumption-based model**. Users pay only for what they use, and operate under an OpEx model.

    -   **Skills**. Less skills required on the operations team.

    -   **Cloud benefits**. You can benefit more from cloud provider knowledge.

    -   **Productivity**. You can focus more on application development than on platform management.

-   Disadvantage
    -   **Platform limitations**. There can be some limitations to a cloud platform that might affect how an application runs.

## SaaS - Software-as-a-Service

In this cloud service model, the cloud provider manages all aspects of the application environment.

-   Advantages

    -   **No CapEx**. Users have no up-front costs.

    -   **Agility**. Users can provide staff with access to the latest software quickly and easily.

    -   **Pay-as-you-go pricing model**. Users can switch to a subscription model.

    -   **Skills**. No deep technical skills are required to deploy, use, and gain the benefits of SaaS.

    -   **Flexibility**. Users can access the same application data from anywhere.

-   Disadvantage
    -   **Software limitations**. There can be some limitations to a software application that might affect how users work.

# Cloud Types

1. Public cloud

    - Services are offered over the public internet and **available to anyone**.
    - Cloud resources are owned and operated by a third-party cloud service provider.
    - Cloud Resources are delivered over the internet.
    - No capital expenditures to scale up.
    - Applications can be quickly provisioned and de-provisioned.
    - Organizations pay only for what they use.

1. Private cloud

    - Computing resources are **used exclusively by users from one business or organization**.
    - Can be physically located at your organization's on-site (on-premises) datacenter, or it can be hosted by a third-party service provider.
    - Hardware must be purchased for start-up and maintenance.
    - Organizations have complete control over resources and security.
    - Organizations are responsible for hardware maintenance and updates.

1. Hybrid cloud

    - A computing environment that combines a public cloud and a private cloud by allowing data and applications to be shared between them.
    - Provides the most flexibility.
    - Organizations determine where to run their applications.
    - Organizations control security, compliance, or legal requirements.

# Azure

## What?

Azure is a continually expanding set of cloud services that help your organization meet your current and future business challenges.

## Why?

-   Offers Support for product development and envisioning
-   Can integrate with your on-premise solutions
-   Offers security backed bu a team of experts
-   provides more than 100 services

## How?

Described very well in this video: [How does Azure work?](https://www.microsoft.com/en-us/videoplayer/embed/RWJKac?postJsllMsg=true)

## Azure Portal

### What?

Is a web-based, unified console that allows you to:

-   Build, manage, and monitor everything from simple web apps to complex cloud deployments.
-   Create custom dashboards for an organized view of resources.
-   Configure accessibility options for an optimal experience.

### Where?

It maintains a presence in every Azure datacenter.

## Azure Marketplace

### What?

[Azure Marketplace](https://azuremarketplace.microsoft.com/) is a "place" where 3rd party companies/individuals offer their solutions and services, which are optimized to run on Azure.

**All solutions and services are certified to run on Azure.**
