---
layout: page
title: Open Source Contributions
permalink: /opensource/
icon: tags
type: page
---

- [Community Projects](#community-projects)
- [Original Projects](#original-projects)
    - [goHTTPForwarder](#gohttpforwarder)
    - [Kubernetes Context Generator](#kubernetes-context-generator)
    - [Go Gitlab Cloud backup](#go-gitlab-cloud-backup)
  - [**Plane Sailing**](#plane-sailing)
  - ["KIP" - **K**eybase **I**dentity **P**rovider](#kip---keybase-identity-provider)
  - [IoT Dashcam & Vehicle Telemetry](#iot-dashcam--vehicle-telemetry)
    - [Dotnet Core SDK Sub Project](#dotnet-core-sdk-sub-project)
  - [PowerShell Modules](#powershell-modules)

## Community Projects
I strive and endeavor to contribute back via either code, issue, feedback or simply feature requests to help others and project owners.    
Open Source projects I've contributed to include;
- [PowerShell Core](https://github.com/powershell)
- [PowerShell DSC community](https://github.com/dsccommunity)
- [Azure CLI](https://github.com/Azure/azure-cli) / [AzCopy](https://github.com/Azure/azure-storage-azcopy)
- Terraform providers e.g. Jira, GitLab
- [MetalLB](https://github.com/metallb/metallb) 
- [Bitnami Helm Charts](https://github.com/bitnami/charts) for External-DNS


As a result of my contributions to the Open Source community, I have earned the [Arctic Code Vault Contributor](https://archiveprogram.github.com/) GitHub 
badge - pretty exciting!


## Original Projects
I generally build open source tooling/scripts to help project productivity and pipelines etc.

The following are some of the more note worthy projects I've built.

#### goHTTPForwarder
Whilst working on a tightly controlled project for a UK Govournment body attempted to improve collaboration, Gitlab Enterprise notification webhooks inherited system-level HTTP proxies which we could not configure.

I built this tool and provisioned in a centralised Kubernetes cluster that could leverage a HTTP Proxy and internet access that would simply accept a Microsoft Teams notification forwarding the request to the Microsoft Teams API via the HTTP Proxy.

For more information visit [https://github.com/rhysjtevans/goHttpForwarder](https://github.com/rhysjtevans/goHttpForwarder) for examples

#### Kubernetes Context Generator
Project: [https://github.com/rhysjtevans/k8s-context](https://github.com/rhysjtevans/k8s-context)
This was built for a project that managed Kubernetes clusters through an in-house service. The tool configured KUBECONFIG based on the management service JSON object contents.

#### Go Gitlab Cloud backup
Accidents happen and I found a use case to build a Go based Gitlab Git repository backup app that would encrypt using GPG and archive the compressed repositories to.

This use case was a great way for me to learn Go and Go Routines multi-thread parallelisation as the tool downloads, compresses and encrypts each git repo individually.

I'm currently still building and thus not made it public yet.
Next iteration will include a Kubernetes operator.


### **Plane Sailing**
I am building a revolutionary DevSecOps accelerator pack called Plane Sailing. The goal of Plane Sailing is to deploy a fully functional DevSecOps team and secure production Kubernetes clusters all in less than a day - very ambitions, right!

This project was born out of frustration with countless engineers/consultancies either reinventing the wheel or waste time building bespoke tooling whilst building a Kubernetes cluster with basic security practices left behind.

Not with a Plane Sailing Kubernetes stack.

The accelerator pack also bridges the gap between technical and management layers providing dashboards for management to track how teams are performing. 
The tool stack will configure & integrate all tools/cloud stacks for peak developer productivity, security whilst providing management with the insight they need to prioritise manage their expectation. 

For more information please visit [inspire.planesailing.io](https://inspire.planesailing.io) including a conception questionnaire - go make an impact! 

### "KIP" - **K**eybase **I**dentity **P**rovider
A Keybase OpenID Connect Identity Provider. This is a serverless app that extends Keybase's vision cryptographically linking corporate identities via OpenID Connect (albeit I used Azure Active Directory) to other online accounts e.g. Twitter, Github, GPG public keys etc.

More information and use cases can be found on the project page [https://github.com/rhysjtevans/kip](https://github.com/rhysjtevans/kip).

It is written in Python and is a serverless (AWS Lambda) design leveraging AWS DynamoDB, API Gateway, AWS Secret Manager, AWS S3, AWS CloudFront and logging via CloudTrail etc.

### IoT Dashcam & Vehicle Telemetry
In my personal time I have built several micro-services and a backend API that is designed to collect data from a Raspberry Pi orchestrated through a `docker-compose` & Git pipeline by [Balena IoT](https://www.balena.io/)

IoT Data collection services include;
 - GPS data, speed, altitude, long, lat etc.
 - Accelerometer & Gyroscope telemetry (every 1/100 sec)
 - Device health monitoring
 - ODBII (Car BUS interface) data collector (Car + Engine health telemetry) - Interesting fact through experimitation newer and some models of cars include pedal positioning!
 - RabbitMQ (incl. Shovel plugin). Provides caching and shipping to a cloud-based RabbitMQ service (TLS+RBAC)
 - Device management client
 - Circular buffer video recorder from two attached cameras (intended for fornt & rear 180° view)

Project is container based to ensure the services are running and healthy incl. MongoDB and MS SQL Server (running on Linux)

#### Dotnet Core SDK Sub Project
Using Dotnet Core (C#) I built and published a basic SDK for the [Balena IoT](https://www.balena.io/) API - [Balena IoT](https://www.balena.io/) have recently forked the project!

### PowerShell Modules
A great achievement was [PSArtifactory](https://github.com/rhysjtevans/PSArtifactory) where I also built a PSDrive interface (leveraging [SHiPS](https://github.com/PowerShell/SHiPS)) for repository traversal

