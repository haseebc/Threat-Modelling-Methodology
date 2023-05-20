# Threat-Modelling-Methodology
# Table of contents

1. [Introduction](#overview)
    1. [In scope](#inscope)
    2. [Out of Scope](#outofscope)
    3. [What is Threat Modelling](#whatis)
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
All associated applications, infrastruction and platform related to the journeys of information and data are considered to be in scope. In addition applicable processess, policies and standards are also in scope where applicable. 

The methodology used is agnostic of the platform, whether this is cloud based, on prem or SaaS. <br>

The rational behind this is threat mdoelling is a multi disciplinary approach and threats can vectors can arise from a wide range of sources. This is irrespective of protocols used in a system being analysed and the underlying technology components. 
### Out of Scope <a name="outofscope"></a>
Quality of systems is not inscope, for instance code quality and efficiences of network protocols is firmly not in scope of this threat modelling methodology.
### What is Threat Modelling <a name="whatis"></a>
As a key cyber security strategy a number of organisations implement technology controls frameworks which require security by design. Security by design can be achieved via threat modelling (TM). TM is considered a inter-disciplinary workshop during which developers, testers, product owners, technicians, operations, application support and security champions work together to perform what is best described as “whiteboard hacking”. The application, infrastructure and platform are torn down and the architecture opened up in detail like a "hacker" would do. Technical vulnerabilities are examined  

There are many variants of threat modelling including full, incremental and semi-automated in cloud CI/CD pipelines. Agile teams should perform “mini” threat modelling as part of creating each user story –thinking of abuse or attack scenarios for assets the software may be handling.

The primary goal is to identify security design flawse arly in the development cycle – to make them less expensive to fix rather than later when they have already been developed. 

This primary  goal cannot be met when full cloud CI/CD is used –as the code is already written –so it is more “semi-automated” threat modelling in this case.While catching design flaws before code is written is the intent, in reality there are many legacy applications which are recommendedto perform a “retro-legacy” threat modelling.  For a “retro-legacy” threat model, this could additionally include some code review of critical areas of the software in legacy applications to check for old crypto, libraries, depreciated function calls, etc.Triggers to identify when a manual Threat Modellingis needed:•A new product is being designed•A legacy applicationhas never had a threat model done yet•A major functionality change or big code modification is made in anapplication•A major vulnerability or security issue has been detected•A threat model hasn’t been done in over 2 years for the application

What might a Threat Model Expose
Findings during TM sessions may for instance indicate ciphers used are forbidden for what is suppose to be a secure cloud connection , tokens used in a application session are open to abuse or the CI CD pipeline is not hardened (secrets exposed in repositoriesd used for a cloud deployment). These findings are assessed in terms of net risk and recommendations for mitigation made.

```bash

Methodology

Metadata and Housekeeping
The TM is timeboxed

Checklist for Threat Modelling

Siziung a Threat model - How long will it take?

A note of Tooling
AI useage. https://github.com/jhaddix/SubreconGTP
Refernces

About the author

