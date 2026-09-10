---
name: New project template
about: Request to on-board a new project to GitHub Actions for IBM Power & IBM Z and
  LinuxONE
title: PROJECT NAME
labels: new-project, p9, z
assignees: pleia2, clnperez, janani66

---

<!--  Please do not leave any questions blank. -->

**Please describe the project**
A clear and concise description of what the project is.

**URL for the project**

**Describe current CI/CD setup**

**Describe the primary use case for the Github Action Runner**
Example: We want to build go libraries for ppc64le. Or run lint tests on s390x.

**Paste a link to the actions workflow file(s), or directory with workflows, you wish to run on this service**
Remember: You'll only want to run workflows that are required for test/build compatibility on ppc64le/s390x.

If the workflow file you wish to run on these architectures doesn't exist yet, you may describe it here.

**How often do you plan on executing the runner?**
For example, every release or every commit.

An educated estimate of how long (5 minutes? 4 hours?) you believe each test may take to run is also valuable here. This estimate can be based on similar tests you already run on other architectures.

**What is the primary programming language for the project?**

**To your knowledge, is this project included in a Product? Which one(s)?**

This can be a product from any company/organization. This question is optional, but can help us report on the value of this service to a broad ecosystem of users.

**Please select desired hardware**

- [ ] Power 9 (ppc64le)
- [ ] IBM Z / LinuxONE (s390x)

<!-- Please update the labels for your selection  -->

**Account names of the GitHub repo admins that will need access to setting up the runner**
