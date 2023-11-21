---
title: AAD Integration
parent: Azure DevOps (ADO)
has_children: false
nav_order: 2
---

## Azure DevOps and Active Directory (AAD) Integration

For enterprises who have Azure Active Directory (AAD) and use it for user management for identity and access to enterprise services. It's key to setup integration between AAD and Azure DevOps (ADO).

This allows for tighter security controls and enabling enterprise security and governance requirements like for example ***Joiners/Movers/Leavers (JML)*** processes.

You can sign in with the same username and password that you use with Microsoft services. Add members to your Azure DevOps organization who are already a part of your work organization. You can also enforce policies for accessing your team's critical resources and key assets.

As members of your AAD are able to create their own ADO organizations using their AAD credentials. It's key when integration with ADO to also restrict the creation of ADO organizations to not lose control and keep within your companies governance and compliance requirements. So restricting creation of organizations needs to be considered. 

The following links can be used to take you to the relevant Microsoft Documentation to achieve this:

- [Connect your organization to AAD](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/connect-organization-to-azure-ad?view=azure-devops)
- [Restrict organization creation with tenant policy in Azure](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/azure-ad-tenant-policy-restrict-org-creation?view=azure-devops)


Additional Links:
- [FAQ's](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/faq-azure-access?view=azure-devops)

