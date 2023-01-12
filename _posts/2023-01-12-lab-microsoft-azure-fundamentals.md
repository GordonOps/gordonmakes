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

There is a clear misalignment between what the learning content writer set out to do, 6 courses and what they actually produced: 3 Learning Paths. Each of the 6 courses linked to one of the 3 paths which made it confusing to get a lay of the land: understanding what material is even being studied. Clicking start and clicking through content on the page lead to literally different courses. I appreciated the opportunity to get extra questions in my study guide but did not appreciate the confusion leading to retracing knowledge I already noted.

Azure thinks it's main value is to build deploy and manage applications, facilitate rapid time to market for features that delight users, and prevent dissapointment with users in a competitive field. What kind of apps: ML/AI, Web 2.0 (JS,Python), and Mobile. Likely also internal tools, big data, and data analytics.

A very interesting video: *"How does Azure Work?* takes the familiar idea of Hypervisor from the last several iterations of windows. Azure datacenters operate big racks of compute hardware with Hypervisors and VMs but adds 2 management components: a **fabric controller** and an **orchestrator**. The orchestrator is communicating with Azure portal or command line, with those commands selects a physical server to execute the commands. The fabric controller recieves Orchestrator commands to then configure and deploy the resources through the hypervisor therein. The video left a good feeling of peeling back the layers of the onion, although it's understandably insufficient to say one has a working understanding.

Azure portal is designed to never go down even for maintainance. Services: compute, networking, storage, mobile cross platform or native apps and notifications, databases multiple engines and mgmt tools, web for building and deploying web apps (eg. azure maps, apis), iot connection and management, big data: for clustering and mass scale analytics, ai services for forecasting and modeling, devops automating software delivery with pipelines that manage integration, deployment, change control.

In the second learning path there is a section of required Sandbox Exercises requesting the learner to perform various administrative tasks. Starts with using the CLI with different interpreters and ends with using the Azure Admin Portal. It was possible to change to bash interpreter by typing bash, and to powershell by typing pwsh easy to remember because it ends like bash with sh for shell. It was also possible to enter an interactive mode which enabled a menu of autocomplete options and gave descriptive colouring to things. I didn't prefer interactive mode because the colouring to me reduced the clarity of what I was seeing.

On regions and zones. Both can contain one or more datacenters. Zones are subdomains of regions which are meant to gaurantee isolation (redundancy concerns). There's also a hedge for loosing your region called a region pair. Finally some sovereign environments require special rules to operate in cooperation with governments and these are called Sovereign Regions. Bemusingly both China North and China East are not maintained by microsoft directly (eyeroll).

Everything provisioned is a resource. Every resource needs to belong to exactly one resource group. Resource groups cannot be nested inside other resource groups. Actions on resource groups affect all the children resource contained therein eg deletion, permission.  Subscriptions have features like identity through Active Directory, enabling azure features linked to predefined billing (boundaries), and are linked to an account to enable provisioning resources. Sub to subscriptions are resource groups with inheritance rules. The structure above subscriptions is management groups with configurable params called governance rules that subscriptions inherit from their parent management group. A VM was created but couldn't be connected to. I suppose this aligns with another lab report so I took some screenshots. Clean up is automatic in the Learn sandbox but in practice deleting the resource group ensure a minimized bill - a good tip. 

## Conclusion
