# Threat-Modelling-Methodology
# Table of contents

1. [Introduction](#overview)
    1. [In scope](#inscope)
    2. [Out of Scope](#outofscope)
    3. [What is Threat Modelling](#whatis)
    4. [When should a Threat Model be Performed](#when)
    5. [What Might a Threat Model Expose](#example)
2. [Methology](#method)


## Introduction
The purpose of this document is to provide an overview of the methodology used for threat modelling of technical systems.
### In Scope <a name="inscope"></a>
All associated applications, infrastructure and platform related to the journeys of information and data are considered to be in scope. In addition applicable processess, policies and standards are also in scope where applicable. 

The methodology used is agnostic of the platform, whether this is cloud based, on prem or SaaS. <br>

The rational behind this is threat mdoelling is a multi disciplinary approach and threats can vectors can arise from a wide range of sources. This is irrespective of protocols used in a system being analysed and the underlying technology components. 
### Out of Scope <a name="outofscope"></a>
Quality of systems is not inscope, for instance code quality and efficiences of network protocols is firmly not in scope of this threat modelling methodology.
### What is Threat Modelling <a name="whatis"></a>
As a key cyber security strategy a number of organisations implement technology controls frameworks which require security by design. Security by design can be achieved via threat modelling (TM). TM is considered a inter-disciplinary workshop during which developers, testers, product owners, technicians, operations, application support and security champions work together to perform what is best described as “whiteboard hacking”. The application, infrastructure and platform are torn down and the architecture opened up in detail like a "hacker" would do. Technical vulnerabilities are examined  
### When Should Threat Modelling be Performed<a name="whatis"></a>
The core objective of TM is to highlight security design weaknesses early within the development cycle – to make them less expensive to fix rather than later when they have already been developed. 

This core goal cannot be achieved when full cloud CI/CD is used because the repositories are already built and written. Hence, automated threat modeling is really not a reality in modern work flows.

So in reality threat modeling can either be done very on in the design phase or performed retrospectively (known as “retro-legacy” threat modelling).  For a “retro-legacy” threat model, this could additionally include some code review of critical areas of the software in legacy applications to check for old crypto, libraries, depreciated function calls, etc.

**Triggers to identify when a manual Threat Modelling is needed:**
+ A new product is being designed
+ A legacy system never had a threat model done yet•A major functionality change or big code modification is made in anapplication
+ A major vulnerability or security issue has been detected
+ A threat model hasn’t been done in over 3 years for the application

### What might a Threat Model Expose <a name="example"></a>
Findings during TM sessions may for instance indicate ciphers used are forbidden for what is suppose to be a secure cloud connection, tokens used in a application session are open to abuse or the CI CD pipeline is not hardened (secrets exposed in repositoriesd used for a cloud deployment). These findings are assessed in terms of net risk and recommendations for mitigation made.

## Methodology<a name="method"></a>
### Threat Modelling Methodology...The Devil is in the Details  

The methodology used is known as Abuser Stories in the industry and the literature.

Abuser Stories are associated to agile ways of working and are to identify security threats in the system. This process of identifying security flaws is done by identifying the ways how the attackers may abuse the system. In Agile modelling, threats modelling process is based on five elements identifying threats, understanding threats, categorizing threats, identifying mitigation strategies and testing. 

Abuse cases are designed to launch an attack on the system and identifying the attack paths of the system. Depending on the systems being assessed some of the work here can be automated; however, the experience of a seasoned trained threat modeller some is a core requirement.

There are many variants of threat modelling including full, incremental and semi-automated in cloud CI/CD pipelines. Agile teams should perform “mini” threat modelling as part of creating each user story –thinking of abuse or attack scenarios for assets the software may be handling.

| Step | Details | Justification |
| :--- | :----------------------------------------------: | :----------------------------------------: |
| 1.1  | Data flow diagram is prepared and reviewed  :white_check_mark:| Ensure there this a technical understanding of how data flows through the components |
| 1.2  | Assets, Controls and Threat Agents identified.   | Critical for understanding the architecture and low level technical control points |
| 2.1  | Ensure purpose and of each flow is understood    | Justification and classification of the flow of data is understood                 |
| 2.2  | Ensudre data transfer&storage crypto understood  | To ensure approved ciphers used for data in transit and storage |
| 2.3  | How is authentication and authorisation achieved?   | Understnding how trust is achieved and IAM model is a critical understanding |
| 2.4 | Are mechanism for secrets stored for data movement?   | For each flow understanding secrets management is required |
| 3.1| Are source code and code dependency scanning implemented  | Securing build phase of the system |
| 3.2 | For cloud is IaC and security policy as code implemented   | Securing cloud infrastructure built and implementing security policy |
| 3.3 | Are built artifacts dynamically scanned for weaknesses  | Provides security assurance of what has been deployed is secure |
| 3.4 | Are built artifacts dynamically scanned for weaknesses  | Provides security assurance of what has been deployed is secure |
| 4.1  | Application security reviewed against OWASP App Sec Verification Standard   | Use of industry standard to validate application security posture |
| 4.2  | Infrastructure and cloud platform security reviewed against CIS benchmarks   | Use of industry standard to validate infra and cloud security posture |
| 5    | Review what auditing and logging employed  | Ensure security event information from systems is captured and alerted upon |
| 6   |    | Ensure there this a technical understanding of how data flows through the components |
| 1    | Data flow diagram is prepared and reviewed   | Ensure there this a technical understanding of how data flows through the components |
| 1    | Data flow diagram is prepared and reviewed   | Ensure there this a technical understanding of how data flows through the components |



Metadata and Housekeeping
The TM is timeboxed

Checklist for Threat Modelling

Siziung a Threat model - How long will it take?

A note of Tooling
AI useage. https://github.com/jhaddix/SubreconGTP
Refernces

About the author

