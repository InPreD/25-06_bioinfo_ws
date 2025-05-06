---
marp: true
theme: default
---

# In-house development and collaboration in InPreD-Norge

3rd Annual workshop on bioinformatics and variant interpretation in InPreD

<https://inpred.github.io/25-06_bioinfo_ws/develop_and_collab>

![bg right](../img/tromso01.png)

---

## Overview

1. Communication channel
2. Project planning
3. Development
4. Issue and bug handling
5. New features

---

![](../img/collaboration_docs01.png)

This is a **private repo** at <https://github.com/InPreD/collaboration_docs> 

---

## 1. Communication channel

### Current situation

- as of today we communicate mainly via email
- some communication via Teams (most of us are "external" lacking some important features features)
- discussions on GitHub via PRs
- we have monthly meetings for updates and discussions

---

## 1. Communication channel

### Future plans

- requirements for platform/service for communication between nodes:
  - open source
  - easy and safe data sharing between nodes
  - free
  - self-hosted
- include bioinformaticians from clinical genetics departments (some of us are involved in CG already)
- currently, we are testing Zulip and Rocket.Chat
- biweekly updates from all nodes

---

## 2. Project Planning

- new projects should be started with a "scoping meeting" were at least one representative of each node
- the following should be discussed and agreed upon:
  - purpose
  - language (default: python)
  - interface (e.g. command line interface, web server)
  - data flow and storage (input and output location, database/filesystem)
  - involved collaborators (which nodes have resources to contribute)
  - deployment options (e.g. baremetal, docker/apptainer)
  - integration with existing projects
  - license (default: GNU AFFERO GENERAL PUBLIC LICENSE - Version 3)
  - intended timeline

---

## 2. Development

### 1. Code should be made available through InPreD group on github

![](../img/github_inpred_group01.png)

---

## 2. Development

### 2. Start off by creating a repository with an empty README.md and LICENSE file, clone it to your local environment and then start developing

![](../img/github_inpred_group01.png)

---

## 2. Development

### 3. Use the agreed branching strategy (suggested: simplified Gitflow workflow)

![](../img/gitflow01.png)

---

- .

## 2. Development

### 4. Commit and push changes early and often to allow others to follow along

![](../img/github_inpred_group01.png)

---

- Follow best practices for the selected programming language. Generally recommended are unit testing (cover test cases from different nodes), keeping functions short, avoid hard-coding, sensible use of packages and libraries.
- Use git commit message conventions.
- Keep the features and PRs small (ideally one PR per feature) to have a tight feedback loop. Focus on one small problem for one feature. Include at least one representative from each node (option to opt out) and set a deadline (e.g. two weeks).
- Pair-programming should be used where it makes sense to enable knowledge and expertise transfer between the different groups.
- Use github actions to test, lint and publish or build your project.
- Provide at least a docker image (can be converted to apptainer) and push them to the inpred group at docker hub.
- Write documentation and check with others that it is understandable.
- Tag and release code that is ready for production using semantic versioning.
