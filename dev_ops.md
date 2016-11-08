# Dev Ops

## What is Dev Ops?

Practices and infrastructure put in place to help developers collaborate and communicate, as well as build, test, and release
software quickly. In reality, Dev Ops is implemented using toolchains, which are sets of tools that take care of the following
components:

1) Code - Code Development, Code Review, Version Control, etc
2) Build - Continuous Integration, builds
3) Test - QA, Regression Testing, Perf Testing, Compatability Testing, etc
4) Package - Artifacts, pre-deploy staging environments
5) Release - Approvals, Release automation, Fallbacks, Change Management
6) Configure - Infra configurations and management such as Servers
7) Monitor - Build Status, Perf Monitoring, UX
8) Collaborate - Version Control, Confluence
9) Communicate - Slack!

An example of a toolchain might look something like this:

1) Code - Github Enterprise
2) Build - Jenkins with CI integration
3) Test - Automated testing built into Tox
4) Package - in-house package and package management solutions like SPM
5) Release - Release standards, Atlassian JIRA to manage Releases
6) Configure - Docker instances on AWS
7) Monitor - in-house monitoring systems with customized UI/UX
8) Collaborate - Atlassian Confluence Docs to manage documentation
9) Communicate - Slack and Private Email Server


