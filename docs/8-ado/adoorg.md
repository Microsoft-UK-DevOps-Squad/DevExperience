---
title: Organization Setup
parent: Azure DevOps (ADO)
has_children: false
nav_order: 1
---

# Azure DevOps Organization

## Overview

There're a number of elements to setting up an ADO organization. Below shows a flowchart with all the key tasks required to setup ADO:

![Setting up Organization](../../assets/devops%20org%20process.png)


# Process to follow

The next section goes through in more detail the steps from above and also provides links to the Microsoft Documentation to help with the setup:

## [Review Business Organizational Structure](https://learn.microsoft.com/en-us/azure/devops/user-guide/plan-your-azure-devops-org-structure?view=azure-devops)

First it's key to understand your business and organizational structure to then use this to drive the ADO setup. This will feed into and inform the next steps. Look the business units, number of applications per business unit and number of developers per business unit. This helps to making decisions around number of organizations and projects that Azure DevOps will need to support.


## [Do I need One or Multiple Organizations?](https://learn.microsoft.com/en-us/azure/devops/user-guide/plan-your-azure-devops-org-structure?view=azure-devops#how-many-organizations-do-you-need)
One organization works for most scenarios and is a good starting point where multiple projects and teams can be added to an organization, which can drive productivity and adoption initially.
Going with a multiple organizations model is generally driven by the need for teams and projects to work in isolation and/or require a different security model across different of a company. 

## [Create Organization](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/create-organization?view=azure-devops)

#### What is an Organization?

- It's the primary entry point (e.g. <https://dev.azure.com/{yourorganization>}) into Azure DevOps where projects and supporting products are hosted.

#### Initial Configuration

- Remember an [Owner](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-organization-ownership?view=azure-devops) for the organization is required.
- URL for logging into the new organization is https://dev.azure.com/{yourorganization}.
- Set [Region](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-organization-location?view=azure-devops) where the organization is hosted.
- Connect your organization to [Azure Active Directory](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/connect-organization-to-azure-ad?view=azure-devops)
- [Restrict Organization](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/azure-ad-tenant-policy-restrict-org-creation?view=azure-devops) create to AAD Tenant

## [Permissions and Access](https://learn.microsoft.com/en-us/azure/devops/organizations/security/access-levels?view=azure-devops)

#### [Review Security Permission Groups](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/add-organization-users?view=azure-devops&tabs=browser)

Learn how to add users to your organization and manage user access through direct assignment.

#### Create Custom Security Permission Groups

- Create ADO Organization Administrator Group
- Create ADO Pipeline Group
- Create ADO Security Administrator Group
- Create ADO Boards Administrator Group

#### Create / Assign AAD Groups to Custom Security Permission Groups

## [Setup Billing for the Organization](https://learn.microsoft.com/en-us/azure/devops/organizations/billing/overview?view=azure-devops)

If you need more than the free tier of resources in your organization, you can set up billing. When you set up billing you can also buy other features offered by Microsoft or other companies.

The free tier offers:
- First five users free (Basic license)
- Azure Pipelines:
    - One Microsoft-hosted CI/CD (one concurrent job, up to 30 hours per month)
    - One self-hosted CI/CD concurrent job
- Azure Boards: Work item tracking and Kanban boards
- Azure Repos: Unlimited private Git repos
- Azure Artifacts: Two GiB free per organization

If move than the above is required, billing will need to be setup for your organization. 

## [Review Security Policies](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops)

Learn how to manage your organization's security policies that determine how applications can access services and resources in your organization. You can access most of these policies in Organization Settings.

## [Setup Auditing and Monitoring](https://devblogs.microsoft.com/devops/introducing-azure-devops-audit-stream/)

- [Enable Log Audit](https://learn.microsoft.com/en-us/azure/devops/organizations/audit/azure-devops-auditing?view=azure-devops&tabs=preview-page) Events
- Create [Audit Stream](https://learn.microsoft.com/en-us/azure/devops/organizations/audit/auditing-streaming?view=azure-devops) to Event Grid / Azure Monitor or Splunk
  
## [Boards](https://learn.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&tabs=agile-process)

Under the Organization Settings for Boards. The processes that are available for projects can be added, updated, deleted and/or disabled in this section. The initial processes that are available are:

- Basic (default)
- Agile
- Scrum
- CMMI

The default process for all new projects can also be set in this section. New Fields, Groups and Pages can be created for the different work item types in the processes. This is key for customizing for your organization.


## [Pipelines]()

Under the Organization Settings for Pipelines. There're a number of options that need to be setup from an organizational perspective. Below are a couple of settings that can be set:

- Creation of [classic build and release pipelines can be disabled](https://devblogs.microsoft.com/devops/disable-creation-of-classic-pipelines/#:~:text=You%20can%20disable%20creation%20of%20classic%20pipelines%20by,creation%20of%20classic%20build%20and%20classic%20release%20pipelines.).
- [Marketplace tasks could be disabled](https://learn.microsoft.com/en-us/azure/devops/pipelines/process/tasks?view=azure-devops&tabs=yaml#disabling-in-box-and-marketplace-tasks).


This is a key area where [Agent Pools](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/pools-queues?view=azure-devops&tabs=yaml%2Cbrowser) need to be setup and managed for the organization. The 2  types of Agents Pools that need to be understood are:

- [Microsoft Hosted Agent Pools](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/hosted?view=azure-devops&tabs=yaml)
    - Can be used for Public deployments
- [Self-Hosted Agent Pools](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/windows-agent?view=azure-devops)
    - Needs to be used when deployments are private and for example go to resources that are private in a Virtual Network.

## [Repositories](https://devblogs.microsoft.com/devops/azure-repos-default-branch-name)

Repositories the default branch name for repositories can for changed. This will affect all new repositories that get created. Currently this is defaulted to **main**


## [Preview Features](https://learn.microsoft.com/en-us/azure/devops/project/navigation/preview-features?view=azure-devops#account-level)

As new features are introduced, you can turn them on or off. That way, you can try them out, provide feedback, and work with the ones that meet your requirements. Some preview features provide access to entire new functionality. Others, such as the New Wiki experience, reflect a change to the user interface, but little or no change in functionality.


