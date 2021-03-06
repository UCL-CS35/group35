---
title: Version Control - Git & GitHub
sidebar: mydoc_sidebar
permalink: /research/version-control/
toc: false
---

We will be using Git for our version control system.

We shortlisted GitHub and Bitbucket as the possible options for hosting our project source codes. Bitbucket is an hosting service for Git repositories. It is attractive to small group (up to 5 members) who want to host their private projects online. GitHub is another hosting service provider but their free plan requires group to keep their code public. As our project’s aim is to make a research study available to the public, our client has no objection on keeping the source code public. By having a public repository, interested developers can submit fixes or new features to improve INcDb. Lastly, GitHub is a also a better option for beginners like us as there is a huge community support available. We decided to use GitHub to host all our source codes and they are available at <https://github.com/UCL-CS35>.

We will be adopting Git Flow for our Git branching model. In our central repo, origin, we will have 2 main branches with infinite lifetime: master and develop. The `origin/master` always reflect a production-ready state. The `origin/develop` always reflect a state with the latest delivered development changes for the next release.

When origin/develop branch is ready to be release, all of the changes will be merged back into `origin/master` and then tagged with a release number. Each time when changes are merged back into `origin/master`, we will automatically build and roll-out our software to our production servers.

We will be using three supporting branches, namely Feature, Release, Hotfix branches. Feature branches may branch off from: develop, must merge back into: develop, has a branch naming convention: anything except `master`, `develop`, `release-`, or `hotfix-`. Feature branches are used to develop new features for the future release. Feature branches exist in developer repos only, not in origin.