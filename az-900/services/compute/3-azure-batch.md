# [Azure Batch](https://docs.microsoft.com/en-us/azure/batch/batch-technical-overview)

Azure Batch enables large-scale parallel and high-performance computing (HPC) batch jobs with the ability to scale to tens, hundreds, or thousands of VMs.

## What is included?

-   Starts a pool of compute VMs for you.
-   Installs applications and staging data.
-   Runs jobs with as many tasks as you have.
-   Identifies failures.
-   Requeues work.
-   Scales down the pool as work completes.
-   At the core of Batch is a high-scale job scheduling engine that’s available to you as a managed service.

## When to use?

-   Batch works well with intrinsically parallel (also known as "embarrassingly parallel") workloads.
    -   These workloads have applications which can run independently, with each instance completing part of the work.
    -   When the applications are executing, they might access some common data.
    -   The application don't communicate with other instances of the application.
