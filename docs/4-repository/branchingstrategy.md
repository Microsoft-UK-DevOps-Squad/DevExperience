---
title: Branching Strategy
parent: Repository
has_children: false
nav_order: 1
---

# Git Branching Strategy


### Intro
The more contributors per project the more important a good branching strategy becomes. Branching strategies depend on:
- the project management
- the project size
- the stakeholders involved
- the production cycle
- the maturity of the team. 

### Git guidance
Git gives you flexibility in how to use version control to share and manage code. The best way to start out is to keep your branch strategy simple. While there are different ways of branching strategies two main concepts are Feature Branches & Release Branches. 


1. Feature Branches
Feature branches are a great way to start green field projects, POCs, or research projects.
- Use feature branches for new features and bug fixes.
- Merge feature branches into the main branch by leveraging reviewers and pull requests.
![Feature branching](./assets/featurebranching.png)


2. Release branches
Release branches are best for projects in production, with a need to roll back to old releases, add updates to release versions or lock relases when they reach their end of life. 
- Create branches to fix bugs from the release branch
- Merge back into the release branches in a pull request.
- Release branches are not merged back into the main branch

[Git Branching Guidance](https://learn.microsoft.com/en-us/azure/devops/repos/git/git-branching-guidance?view=azure-devops)
A best practice case study e how Microsoft does branching is [here](https://learn.microsoft.com/en-us/devops/develop/how-microsoft-develops-devops).
  
