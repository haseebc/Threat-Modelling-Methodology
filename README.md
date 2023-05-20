# Threat-Modelling-Methodology
# Table of contents

1. [Introduction](#overview)
    1. [In scope](#inscope)
    2. [Gem files to add](#gems)
2. [Frontend](#frontend)
    1. [Views](#views)
3. [Routes](#routes)
4. [Controller](#controller)
5. [Models](#model)
    1. [checks table](#checks)
6. [Attack Engine](#attackengine)
    1. [Attack Calls](#attackcalls)
7. [Java Scripts Used](#js)
    1. [Timer check for script to run](#timerjs)
8. [Redis and Heroku](#redisandheroku)
    1. [Useful Heroku comamnds](#herokucommands)
    2. [Sidekiq overview and how to deploy to Heroku](#sidekiq)
    23. [Sidekiq overview and how to deploy to Heroku](#sidekiq)
9. [Developing & Deploying](#developdeploy)

## Introduction
The purpose of this document is to provide an overview of the methodology used for threat modelling of technical systems.
### In Scope <a name="inscope"></a>
All associated applications, infrastruction and platform related to the journeys of information and data are considered to be in scope. In addition applicable processess, policies and standards are also in scope where applicable. The methodology used is agnostic of the platform, whether this is cloud based, on prem or SaaS. 
The rational behind this is threat mdoelling is a multi disciplinary approach and threats can vectors can arise from a wide range of sources. This is irrespective of protocols used in a system being analysed and the underlying technology components. 
### Out of Scope <a name="Out of Scope"></a>
Quality of systems is not inscope, for instance code quality and efficiences of network protocols is firmly not in scope of this threat modelling methodology.

```bash
