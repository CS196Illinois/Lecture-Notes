# Dev Ops

## What is Dev Ops?

Practices and infrastructure put in place to help developers collaborate and communicate, as well as build, test, and release
software quickly. In reality, Dev Ops is implemented using toolchains, which are sets of tools that take care of the following
components:<br>

1) Code - Code Development, Code Review, Version Control, etc <br>
2) Build - Continuous Integration, builds<br>
3) Test - QA, Regression Testing, Perf Testing, Compatability Testing, etc<br>
4) Package - Artifacts, pre-deploy staging environments<br>
5) Release - Approvals, Release automation, Fallbacks, Change Management<br>
6) Configure - Infra configurations and management such as Servers<br>
7) Monitor - Build Status, Perf Monitoring, UX<br>
8) Collaborate - Version Control, Confluence<br>
9) Communicate - Slack!<br>

An example of a toolchain might look something like this:<br>

1) Code - Github Enterprise<br>
2) Build - Jenkins with CI integration<br>
3) Test - Automated testing built into Tox<br>
4) Package - in-house package and package management solutions like SPM<br>
5) Release - Release standards, Atlassian JIRA to manage Releases<br>
6) Configure - Docker instances on AWS<br>
7) Monitor - in-house monitoring systems with customized UI/UX<br>
8) Collaborate - Atlassian Confluence Docs to manage documentation<br>
9) Communicate - Slack and Private Email Server<br>

## Things you should already know

### Version Control
### Communication

## Things you might not know

### Code Review
### Continuous Integration
### Build Tools
### Different Types of Testing
### Testing Libraries and Implementation
### Packaging
### Release Management
### Server and Infra Configuration
### Performance Monitoring
### Documentation

# Dev Ops Issues to Think About


## Code / Test
### How do you measure code quality?
1) Analysis in production <br>
2) pre-production code profiling<br>
3) static code analysis<br>
4) unit tests<br>
5) code coverage based on bugs found by users<br>
6) conduct code reviews<br>

### How do you manage technical debt?
1) Emphasis on refactoring, replacing, and modernizing legacy code
2) Avoid technical debt at all costs using architecture design and review?
3) Strategically incur short-term technical debt to enable experimentation and fast feedback?
4) Track and measure short-term technical debt and pay it off ASAP?
5) Keep track of high-cost technical debts in backlogs
6) Do you suffer from technical debt as a result of legacy application development or lack of quality control in the past?

### How is your code managed and versioned?
1) Distributed Version Control
2) Shared network drives and backups
3) open source sharing systems, server-based sharing systems
4) Google Docs!


## Build
### Build Tools (Tools that automatically generate executables from source. ie apk's for android)
Build Automation scripts and automates activities that programers have to do often like:

1) Downloading dependencies
2) compiling source into binary
3) Packaging binary
4) Running Tests
5) Automatically Deploy to prod

What build tools are you using? What testing frameworks?

### Continuous Integration
1) Do you have continuous integration?
2) Does it automatically deploy to prod?
3) What conditions does the build fail?
4) In-house solutions or SaaS?

### Automation
1) on-demand: builds through a user running a script on the command line
2) scheduled: CI server, nightly builds, regular CRON jobs
3) triggered: Triggered on commit to VCS? 

## Package and Dependency Management
### What Package Manager do you use?
1) In-house package manager (SPM)
2) Public or open source package manager?

### How do you manage dependencies and versioning?
1) Maintain artifact repository with the latest binaries which all teams use
2) Work item tracking system 
3) Versioned interfaces between different services
4) Track versions in google docs or a spreadsheet

## Release
## Configure
## Monitor
### How are issues in prod reported to dev teams?
1) In-house instrumentation generates automated alerts to all relevant teams
2) SaaS issue tracking tools that are available to all relevant teams in real-time
3) End-user requests and complaints via direct contact
4) We don't find out until its too late :(




## Issues and Testing
### How are Issues in Prod reported to dev teams?
Instrumentation


# Why Dev Ops is important

## Exhibit A: Uber










