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

1. Regions give you the flexibility to bring applications closer to your users no matter where they are. In other words, they help you improve the **performance** of your application.
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

Not every region has support for availability zones. You can find a list of [Azure regions with availability zones here.](https://docs.microsoft.com/en-us/azure/availability-zones/az-region#azure-regions-with-availability-zones)

## Why?

1. **Run mission-critical** applications and build **high-availability** into your application architecture by co-locating your compute, storage, networking, and data resources within a zone and **replicating** data in other zones.

## Types of services

-   **Zonal services**: You pin the resource to a specific zone.
-   **Zone-redundant services**: The platform replicates automatically across zones.
-   **Non-regional services**: Services are always available from Azure geographies and are resilient to zone-wide outages as well as region-wide outages.
