---
title: Branch Policies
parent: Repository
has_children: false
nav_order: 3
---

## Branch Policies

This section attempts to provide some practical guidence of implementing branch policies with an opinionated set of questions to run through. The reality is that branch policies are certainly needed to support governance, security and maintain a working version of the code but they have the potential to slow down a team and impact delivery. This topic therefore must incorporate others across people, process and technology. It is not a standalone, rather a part of the puzzle. 

---

## Documentation

* [Azure DevOps](https://learn.microsoft.com/en-us/azure/devops/repos/git/branch-policies-overview?view=azure-devops)
* [GitHub Actions](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule)

---

## Considerations

Consider why you are looking to use branch policies as there are different types. You may be looking at enforcing release or behaviour constraints such as pull requests or ensuring code quality markers are hit such as passing automated tests or code styling.

Security and governance plays a key part here to prevent accidental or unauthorized changes to critical branches such as the main branch. Check the [branching strategies](./branchingstrategy.md) for more info here.

---

## Questions to Ask

These questions can help define the approach and branching policies that you would want to apply:

* Are you looking to provide traceability of end-to-end requirements to code?
  * [Check for linked work items](https://learn.microsoft.com/en-us/azure/devops/repos/git/branch-policies?view=azure-devops&tabs=browser#check-linked-wi)

* Are you wanting to enforce code quality through review and/or automated SAST tooling?
  * [Comment Resolution](https://learn.microsoft.com/en-us/azure/devops/repos/git/branch-policies?view=azure-devops&tabs=browser#check-comment-resolution)
  * [Build Validation](https://learn.microsoft.com/en-us/azure/devops/repos/git/branch-policies?view=azure-devops&tabs=browser#build-validation)
  * [Status Checks](https://learn.microsoft.com/en-us/azure/devops/repos/git/branch-policies?view=azure-devops&tabs=browser#require-approval-from-external-services)

The same policies can be applied for GitHub as Azure DevOps: [here](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule#creating-a-branch-protection-rule).


---

## An Opinionated Starting Point

This is a good baseline starting point for policies for a team getting into DevOps and on their journey to DevOps maturity. As the team starts to increase their developer velocity and gain maturity they can add more automation and reduce the amount of manual checks involved in their release cycle. 

* Use pull requests and require code reviews - this requires that the team consider their process surrounding this to ensure that members are not 'waiting' on someone to approve but helps with ensuring that code changes are lightweight and contained. Consider the [branching strategies](./branchingstrategy.md) and how feature branches are used here. 

* Add build validation policies - You want to know that your code is building and functional through unit tests. As you mature you can add in additional validation and status checks for tasks such as automated integration testing, SAST and DAST scanning etc.