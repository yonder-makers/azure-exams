# Cloud Computing

## What?

It's the delivery of computing services over the internet, which is otherwise known as the cloud.

## Why?

-   Lower your operating costs.
-   Run your infrastructure more efficiently.
-   Scale as your business needs change.
-   Teams deliver new features to their users at record speeds.
-   Users expect an increasingly rich and immersive experience with their devices and with software.
-   You have access to:
    -   A nearly limitless pool of raw compute, storage, and networking components.
    -   Speech recognition and other cognitive services that help make your application stand out from the crowd.
    -   Analytics services that deliver telemetry data from your software and devices.

# Cloud Models

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

# Azure Services

![Available Services](https://docs.microsoft.com/en-us/learn/azure-fundamentals/intro-to-azure-fundamentals/media/azure-services-6c41a736.png)

## 1. Compute

These are services that offer Computational Power (CPU & RAM).

1. Azure Virtual Machines

    Windows or Linux virtual machines (VMs) hosted in Azure.

1. Azure Virtual Machine Scale Sets

    Scaling for Windows or Linux VMs hosted in Azure.

1. Azure Kubernetes Service

    Cluster management for VMs that run containerized services.

1. Azure Service Fabric

    Distributed systems platform that runs in Azure or on-premises.

1. Azure Batch

    Managed service for parallel and high-performance computing applications.

1. Azure Container Instances

    Containerized apps run on Azure without provisioning servers or VMs.

1. Azure Functions

    An event-driven, serverless compute service.

## 2. Networking

Linking compute resources and providing access to applications is the key function of Azure networking.

1. Azure Virtual Network

    Connects VMs to incoming virtual private network (VPN) connections.

1. Azure Load Balancer

    Balances inbound and outbound connections to applications or service endpoints.

1. Azure Application Gateway

    Optimizes app server farm delivery while increasing application security.

1. Azure VPN Gateway

    Accesses Azure Virtual Networks through high-performance VPN gateways.

1. Azure DNS

    Provides ultra-fast DNS responses and ultra-high domain availability.

1. Azure Content Delivery Network

    Delivers high-bandwidth content to customers globally.

1. Azure DDoS Protection

    Protects Azure-hosted applications from distributed denial of service (DDOS) attacks.

1. Azure Traffic Manager

    Distributes network traffic across Azure regions worldwide.

1. Azure ExpressRoute

    Connects to Azure over high-bandwidth dedicated secure connections.

1. Azure Network Watcher

    Monitors and diagnoses network issues by using scenario-based analysis.

1. Azure Firewall

    Implements high-security, high-availability firewall with unlimited scalability.

1. Azure Virtual WAN

    Creates a unified wide area network (WAN) that connects local and remote sites.

## 3. Storage

1. Azure Blob storage

    Storage service for very large objects, such as video files or bitmaps.

1. Azure File storage

    File shares that can be accessed and managed like a file server.

1. Azure Queue storage

    A data store for queuing and reliably delivering messages between applications.

1. Azure Table storage

    Table storage is a service that stores non-relational structured data (also known as structured NoSQL data) in the cloud, providing a key/attribute store with a schemaless design.

These services all share several common characteristics:

-   Durable and highly available with redundancy and replication.
-   Secure through automatic encryption and role-based access control.
-   Scalable with virtually unlimited storage.
-   Managed, handling maintenance and any critical problems for you.
-   Accessible from anywhere in the world over HTTP or HTTPS.

## 4. Mobile

Back-end service for Mobile Applications.
They can have the following features:

-   Adding corporate sign-in.
-   Connecting to on-premises resources such as SAP, Oracle, SQL Server, and SharePoint made simple.
-   Offline data synchronization.
-   Connectivity to on-premises data.
-   Broadcasting push notifications.
-   Autoscaling to match business needs.

## 5. Databases

1. Azure Cosmos DB

    Globally distributed database that supports NoSQL options.

1. Azure SQL Database

    Fully managed relational database with auto-scale, integral intelligence, and robust security.

1. Azure Database for MySQL

    Fully managed and scalable MySQL relational database with high availability and security.

1. Azure Database for PostgreSQL

    Fully managed and scalable PostgreSQL relational database with high availability and security.

1. SQL Server on Azure Virtual Machines

    Service that hosts enterprise SQL Server apps in the cloud.

1. Azure Synapse Analytics

    Fully managed data warehouse with integral security at every level of scale at no extra cost.

1. Azure Database Migration Service

    Service that migrates databases to the cloud with no application code changes.

1. Azure Cache for Redis

    Fully managed service caches frequently used and static data to reduce data and application latency.

1. Azure Database for MariaDB

    Fully managed and scalable MariaDB relational database with high availability and security.

## 6. Web

1. Azure App Service

    Quickly create powerful cloud web-based apps.

1. Azure Notification Hubs

    Send push notifications to any platform from any back end.

1. Azure API Management

    Publish APIs to developers, partners, and employees securely and at scale.

1. Azure Cognitive Search

    Deploy this fully managed search as a service.

1. Web Apps feature of Azure App Service

    Create and deploy mission-critical web apps at scale.

1. Azure SignalR Service

    Add real-time web functionalities easily.

## 7. Internet of Things

1. IoT Central

    Fully managed global IoT software as a service (SaaS) solution that makes it easy to connect, monitor, and manage IoT assets at scale.

1. Azure IoT Hub

    Messaging hub that provides secure communications between and monitoring of millions of IoT devices.

1. IoT Edge

    Fully managed service that allows data analysis models to be pushed directly onto IoT devices, which allows them to react quickly to state changes without needing to consult cloud-based AI models.

## 8. Big Data

1. Azure Synapse Analytics

    Run analytics at a massive scale by using a cloud-based enterprise data warehouse that takes advantage of massively parallel processing to run complex queries quickly across petabytes of data.

1. Azure HDInsight

    Process massive amounts of data with managed clusters of Hadoop clusters in the cloud.

1. Azure Databricks

    Integrate this collaborative Apache Spark-based analytics service with other big data services in Azure.

## 9. AI

1. Azure Machine Learning Service

    A cloud-based environment you can use to develop, train, test, deploy, manage, and track machine learning models. It can auto-generate a model and auto-tune it for you. It will let you start training on your local machine, and then scale out to the cloud.

1. Azure ML Studio

    Collaborative visual workspace where you can build, test, and deploy machine learning solutions by using prebuilt machine learning algorithms and data-handling modules.

1. Cognitive Services

    1. Vision

        Use image-processing algorithms to smartly identify, caption, index, and moderate your pictures and videos.

    1. Speech

        Convert spoken audio into text, use voice for verification, or add speaker recognition to your app.

    1. Knowledge mapping

        Map complex information and data to solve tasks such as intelligent recommendations and semantic search.

    1. Bing Search

        Add Bing Search APIs to your apps and harness the ability to comb billions of webpages, images, videos, and news with a single API call.

    1. Natural Language processing

        Allow your apps to process natural language with pre-built scripts, evaluate sentiment, and learn how to recognize what users want.

## 10. DevOps

1. Azure DevOps

    Use development collaboration tools such as high-performance pipelines, free private Git repositories, configurable Kanban boards, and extensive automated and cloud-based load testing. Formerly known as Visual Studio Team Services.

1. Azure DevTest Labs

    Quickly create on-demand Windows and Linux environments to test or demo applications directly from deployment pipelines.
