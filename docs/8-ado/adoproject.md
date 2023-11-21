---
title: Projects
parent: Azure DevOps (ADO)
has_children: false
nav_order: 3
---

# Azure DevOps Projects


## Overview

An organization can have multiple projects and it's key to look at the project structure. Asking questions like:
- Do we need one project per Team?
- Do we need one project per Business Area?
- Do we need one project per product?
- How do we collaborate across teams and projects?
- How much organizational structure change do we expect?

The questions above start to build out a picture that informs the Azure DevOps project and also can impact the organization design. As if there's a lot of organizational structure change. How would you make sure the Azure DevOps design can handle it without a lot of redesign and moving projects and teams around?

Some examples:
- By creating a project per Business Process Area (e.g. Payments) if the names and structure of the organization changes the Payments BPA project should still be valid including the team membership.

## [Project](https://docs.microsoft.com/en-us/azure/devops/organizations/projects/about-projects?view=azure-devops)

Below shows some of the key steps that need to be followed to setup an ADO Project for an Organization.

![Projects](../../assets/devops%20projects%20process.png)
    
- Define process for Access, Roles and Permissions at Project and Team level prior to creation of first project. (tbc - build out more info)
    - Roles and Responsibilities (tbc)
- Define process for Service Connections and Agent Pools
- [Create Project](https://learn.microsoft.com/en-us/azure/devops/organizations/projects/create-project?view=azure-devops&tabs=browser)
- [Structure your Project](https://learn.microsoft.com/en-us/azure/devops/organizations/projects/about-projects?view=azure-devops#structure-your-project)
- [Add Team to your Project](https://learn.microsoft.com/en-us/azure/devops/organizations/projects/about-projects?view=azure-devops#when-to-add-a-team-scaling-agile-tools-across-the-enterprise)

## [Teams](https://docs.microsoft.com/en-us/azure/devops/organizations/settings/about-teams-and-settings?view=azure-devops)
   - Each project gets a default team created.
   - Optional, create any additional teams required for the project an/or identified in the planning your organization structure section above.
   - Define process for Access, Roles and Permissions at Team level (tbc - build out more info)
      - Roles and Responsibilities (tbc)
   - [Manage and configure team tools](https://learn.microsoft.com/en-us/azure/devops/organizations/settings/manage-teams?toc=%2Fazure%2Fdevops%2Fget-started%2Ftoc.json&bc=%2Fazure%2Fdevops%2Fget-started%2Fbreadcrumb%2Ftoc.json&view=azure-devops) 


## [Boards](https://docs.microsoft.com/en-us/azure/devops/boards/get-started/what-is-azure-boards?view=azure-devops)

Azure Boards is a web-based service that enables teams to plan, track, and discuss work across the entire development process, while it supports agile methodologies, including Scrum and Kanban. Azure Boards provides a customizable platform for managing work items, allowing teams to collaborate effectively and streamline their workflow. Sign up, customize, and experience the benefits of using Azure Boards.

Below shows some of the configuration steps to follow to get Boards setup in a Project:
- Review process's setup in the Organization.
    - [About areas and iteration paths](https://learn.microsoft.com/en-us/azure/devops/organizations/settings/about-areas-iterations?toc=%2Fazure%2Fdevops%2Freference%2Ftoc.json&bc=%2Fazure%2Fdevops%2Freference%2Fbreadcrumb%2Ftoc.json&view=azure-devops)
- Configure the Team configuration for Backlogs, working days, bugs, iterations, areas and templates.
- Optional, setup GitHub connection for linking Boards to a GitHub repo.
    - [Overview](https://learn.microsoft.com/en-us/azure/devops/cross-service/github-integration?view=azure-devops)
    - [Azure Boards - GitHub Integration](https://learn.microsoft.com/en-us/azure/devops/boards/github/?view=azure-devops)
- Config the Teams Board for their ways of working (e.g. workflow, swim-lanes, styles and fields)

## [Repositories](https://docs.microsoft.com/en-us/azure/devops/repos/git/create-new-repo?toc=%2Fazure%2Fdevops%2Forganizations%2Ftoc.json&bc=%2Fazure%2Fdevops%2Forganizations%2Fbreadcrumb%2Ftoc.json&view=azure-devops)

A project can have one or many repositories. It's key to look at your working patterns and go with what would work for your project team. The trend is to drive agility and quicker smaller changes into Production. So, this needs to be taken into account with the repository strategy for the project.

Below are a few tasks to go through when settings up a repository of an ADO Project:
- Define and [branching strategy](../4-repository/branchingstrategy.md) for the Team when working with a repo.
- Set default branch name (e.g. main)
- Apply policies to the repo.
- Review and apply security groups and roles to repo.
- Developer team to agree approach to repo's for their applications:
    - One vs. many
    - Shared vs. Forked
- Define process for Access, Roles and Permissions at repo level based on above requirements.
- [Create Repo](https://learn.microsoft.com/en-us/azure/devops/repos/git/create-new-repo?view=azure-devops)

## [Pipelines](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/what-is-azure-pipelines?view=azure-devops)
![Pipelines](../../assets/devops%20pipelines%20process.png)

Best practice is to move to YAML pipelines for both build and release pipelines. This allows for managing the pipelines as code and storing them in repos to drive consistency and audibility linked to builds and releases.

Pipelines run on [Agent Pools](https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/pools-queues?toc=%2Fazure%2Fdevops%2Forganizations%2Ftoc.json&bc=%2Fazure%2Fdevops%2Forganizations%2Fbreadcrumb%2Ftoc.json&view=azure-devops&tabs=yaml%2Cbrowser), so when creating a pipeline an agent pool needs to be available to execute the pipeline. For security and scalability its recommended  to use self-hosted agents for pipelines, but Microsoft Hosted-Agents can be used, but can't deploy into private environments.

[Create first pipeline](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops) using the agent pool created above and start to expand by creating more agent pools and pipelines to meet your business needs.

