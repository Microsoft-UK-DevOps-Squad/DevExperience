---
title: Overview
nav_order: 1
---

# E2E Develover Experience Guide
This Developer Guide will guide you through the concepts and setup of Microsoft DevOps tooling, from decision making to good practices. It is designed to bring customer and partners to a good (Level 200) knowledge of Developer Experience tooling. It is meant as decision guidance and practical insights to the Microsoft DevOps tooling. All instructions provided require a basic understanding of  [DevOps](https://learn.microsoft.com/en-us/devops/what-is-devops)

## The following areas will be covered
- Setup and automation of Project Management
- Insights into different development environments
- Guidance for Repositories & Branching
- Creating automated CI/CD pipelines
- Adding security to the E2E Developer Lifecycle
- Leveraging AI for coding & development
- Going deeper into set ups for Azure DevOps (ADO) & GitHub (GH)




## Diagram of E2E Developer Architecture 

![Diagram](/assets/DevOps%20Workflow.png)


### Legend
1. Git Branching – Keep your branching strategy simple; start basic and extend as required.
2. Use Pull Requests & Enforce with Branch Policies
3. Enable approvals & checks for deployments and service connections
4. Implement Continuous Integration
  - Execute unit tests as part of the CI process
  - Enable static application security testing e.g. SonarCloud
  - [PREVIEW] Enable Defender for DevOps  
5. Implement Continuous Delivery
  - Use Feature Flags for progressive exposure of features/experiments
  - Use Infrastructure-as-Code to provision resources and manage configuration
6. Perform Continuous Monitoring
  - Use Application Insights if appropriate 

---

## Contributors

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"/></a>
  </li>
{% endfor %}
</ul>

---

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft trademarks or logos is subject to and must follow [Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general). Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship. Any use of third-party trademarks or logos are subject to those third-party's policies.
