---
title: ADO Organization/s Setup
parent: DevOps Setup
has_children: false
nav_order: 2
---

# Azure DevOps Organization/s Setup

## Overview

There're a number of elements to setting up an ADO organization. 

Below shows a flowchart with all the key tasks required to setup ADO:

![Setting up Organization](../../assets/devops%20org%20process.png)


## Process to follow

The next section goes through in more detail the steps from above and also provides links to the Microsoft Documentation to help with the setup:

### STEP 1 - [Review Business Organizational Structure](https://learn.microsoft.com/en-us/azure/devops/user-guide/plan-your-azure-devops-org-structure?view=azure-devops)

First it's key to understand your business and organizational structure to then use this to drive the ADO setup. This will feed into and inform the next steps.

Look the business units, number of applications per business unit and number of developers per business unit.

This helps to making decisions around number of organizations and projects that Azure DevOps will need to support.


### STEP 2 - [Do I need One or Multiple Organizations?](https://learn.microsoft.com/en-us/azure/devops/user-guide/plan-your-azure-devops-org-structure?view=azure-devops#how-many-organizations-do-you-need)
One organization works for most scenarios and is a good starting point where multiple projects and teams can be added to an organization, which can drive productivity and adoption initially.
Going with a multiple organizations model is generally driven by the need for teams and projects to work in isolation and/or require a different security model across different of a company. 

### STEP 3 - [Create Organization](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/create-organization?view=azure-devops)

#### What is an Organization?

- It's the primary entry point (e.g. <https://dev.azure.com/{yourorganization>}) into Azure DevOps where projects and supporting products are hosted.

#### Initial Configuration

- Remember an [Owner](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-organization-ownership?view=azure-devops) for the organization is required.
- URL for logging into the new organization is https://dev.azure.com/{yourorganization}.
- Set [Region](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-organization-location?view=azure-devops) where the organization is hosted.
- Connect your organization to [Azure Active Directory](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/connect-organization-to-azure-ad?view=azure-devops)
- [Restrict Organization](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/azure-ad-tenant-policy-restrict-org-creation?view=azure-devops) create to AAD Tenant

### STEP 4 - [Permissions and Access](https://learn.microsoft.com/en-us/azure/devops/organizations/security/access-levels?view=azure-devops)

#### [Review Security Permission Groups](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/add-organization-users?view=azure-devops&tabs=browser)

Learn how to add users to your organization and manage user access through direct assignment.

#### Create Custom Security Permission Groups

- Create ADO Organization Administrator Group
- Create ADO Pipeline Group
- Create ADO Security Administrator Group
- Create ADO Boards Administrator Group

#### Create / Assign AAD Groups to Custom Security Permission Groups

### STEP 5 - [Setup Billing for the Organization](https://learn.microsoft.com/en-us/azure/devops/organizations/billing/overview?view=azure-devops)

### STEP 6 - [Review Security Policies]()

### STEP 7 - [Setup Auditing and Monitoring](https://devblogs.microsoft.com/devops/introducing-azure-devops-audit-stream/)

- [Enable Log Audit](https://learn.microsoft.com/en-us/azure/devops/organizations/audit/azure-devops-auditing?view=azure-devops&tabs=preview-page) Events
- Create [Audit Stream](https://learn.microsoft.com/en-us/azure/devops/organizations/audit/auditing-streaming?view=azure-devops) to Event Grid / Azure Monitor or Splunk
  
### 

