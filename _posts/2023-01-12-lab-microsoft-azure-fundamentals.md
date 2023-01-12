---
layout: post
title: 'Lab: Microsoft Azure Fundam.s'
date: 2023-01-12 10:57 -0500
categories: lab
---
## Abstract
As my college program begins the course MS Azure 1: Azure Administration we open with a unit based on the AZ-900 series of Learning Paths on *learn.microsoft.com*. Next week we take on the AZ104 preparatory material which leads to the Azure Administrator Associate level Exam. 

The Learning Goals for the series are quoted below:
> After completing this learning path, you'll be able to:
>
>* Understand the benefits of cloud computing in Azure and how it can save you time and money
>* Explain cloud concepts such as high availability, scalability, elasticity, agility, and disaster recovery
>* Describe core Azure architecture components such as subscriptions, management groups, resources and resource groups
>* Summarize geographic distribution concepts such as Azure regions, region pairs, and availability zones

## Method
This lab is essentially to review the material in these 6 curriculum subjects are provided by Learn.Microsoft.com in 3 Learning Paths.

1. [Describe core Azure concepts](https://learn.microsoft.com/en-us/training/paths/az-900-describe-cloud-concepts/)
2. [Describe Azure architecture and services](https://learn.microsoft.com/en-us/training/paths/azure-fundamentals-describe-azure-architecture-services/)
3. [Describe Azure management and governance](https://learn.microsoft.com/en-us/training/paths/describe-azure-management-governance/)

## Observations

There is a clear misalignment between what the learning content writer set out to do, 6 courses and what they actually produced: 3 Learning Paths. Each of the 6 courses linked to one of the 3 paths which made it confusing to get a lay of the land: understanding what material is even being studied. 

Azure thinks it's main value is to build deploy and manage applications, facilitate rapid time to market for features that delight users, and prevent dissapointment with users in a competitive field. What kind of apps: ML/AI, Web 2.0 (JS,Python), and Mobile. Likely also internal tools, big data, and data analytics.

A very interesting video: *"How does Azure Work?* takes the familiar idea of Hypervisor from the last several iterations of windows. Azure datacenters operate big racks of compute hardware with Hypervisors and VMs but adds 2 management components: a **fabric controller** and an **orchestrator**. The orchestrator is communicating with Azure portal or command line, with those commands selects a physical server to execute the commands. The fabric controller recieves Orchestrator commands to then configure and deploy the resources through the hypervisor therein. The video left a good feeling of peeling back the layers of the onion, although it's understandably insufficient to say one has a working understanding.



## Conclusion