# Threat-Modelling-Methodology
# Table of contents

1. [Introduction](#overview)
    1. [In scope](#inscope)
    2. [Out of Scope](#outofscope)
    3. [What is Threat Modelling](#whatis)
    4. [When should a Threat Model be Performed](#when)
    5. [What Might a Threat Model Expose](#example)
2. [Methology](#method)
    1. [Abuser User Stories Threat Modelling, Devis is in the Detail](#abuser)
    2. [Threat Modelling Checklist](#checklist)
    3. [Tooling](#tooling)
2. [About the Author](#about)


## Introduction
The purpose of this document is to provide an overview of the methodology used for threat modelling of technical systems.
### In Scope <a name="inscope"></a>
All associated applications, infrastructure and platform related to the journeys of information and data are considered to be in scope. In addition processess, policies and standards are also in scope where applicable. 

The rational behind this is that threat mdoelling is a multi disciplinary approach and attack vectors can arise from a wide range of sources. This is irrespective of protocols used in a system being analysed and the underlying technology components. 
### Out of Scope <a name="outofscope"></a>
Quality of systems is not inscope, for instance code quality and efficiences of network protocols is firmly not in scope of this threat modelling methodology.
### What is Threat Modelling <a name="whatis"></a>
As a key cyber security strategy a number of organisations implement technology controls frameworks which require security by design. Security by design can be achieved via threat modelling. Threat modelling is considered a inter-disciplinary workshop during which developers, testers, product owners, technicians, operations, application support and security champions work together to perform what is best described as “whiteboard hacking”. The application, infrastructure and platform are torn down and the architecture opened up in detail like a "hacker" would do. Technical vulnerabilities are examined  
### When Should Threat Modelling be Performed<a name="whatis"></a>
The core objective of threat modelling is to highlight security design weaknesses early within the development cycle – to make them less expensive to fix rather than later when they have already been developed. 

This core goal cannot be achieved when full cloud CI/CD is used because the repositories are already built and written. Hence, automated threat modeling is really not a reality in modern work flows.

So in practice, threat modeling can either be done very early on in the design phase or performed retrospectively (known as “retro-legacy” threat modelling).  For a “retro-legacy” threat models, this could additionally include some code review of critical areas of the software in legacy applications to check for old crypto, libraries, depreciated function calls, etc.

**Triggers to identify when a manual Threat Modelling is needed:**
+ A new product is being designed
+ A legacy system never had a threat model done yet
+ A major functionality change or big code modification is made in a system
+ A major vulnerability or security issue has been detected
+ A threat model hasn’t been done in over 3 years for the application

### What might a Threat Model Expose <a name="example"></a>
Findings during threat modelling sessions may for instance indicate ciphers used are forbidden for what is suppose to be a secure cloud connection, tokens used in a application session are open to abuse or the CI CD pipeline is not hardened (secrets exposed in repositoriesd used for a cloud deployment). These findings are assessed in terms of net risk and recommendations for mitigation made.

## Methodology<a name="method"></a>
### Threat Modelling Methodology...The Devil is in the Details  <a name="method"></a>

The methodology used is known as Abuser Stories in the industry and the literature.

This methodology used is agnostic of the platform, whether this is cloud based, on prem or SaaS. In reality system are often a combination of third party components (SaaS), specific cloud build environment with often connectivity to on premise datacentres.

Abuser Stories are associated to agile ways of working and are to identify security threats in the system. This process of identifying security flaws is done by identifying the ways how the attackers may abuse the system. In Agile modelling, threats modelling process is based on five elements identifying threats, understanding threats, categorizing threats, identifying mitigation strategies and testing. 

Abuse cases are designed to launch an attack on the system and identifying the attack paths of the system. Depending on the systems being assessed some of the work here can be automated; however, the experience of a seasoned trained threat modeller some is a core requirement.

There are many variants of threat modelling including full, incremental and semi-automated in cloud CI/CD pipelines. Agile teams should perform “mini” threat modelling as part of creating each user story –thinking of abuse or attack scenarios for assets the software may be handling.

The methodology is time boxed, meaning a specific amount of time (number of days) is allocated to the excercise with some flexibility. As mentioned above threat modelling is a collaborative approach whether the threat modelling leader invites technical experts to assist with tearing down the system during white boarding with a heacker mentality.

### Threat Modelling Checklist<a name="abuser"></a> 
Detailed below is a overall checklist of a possible threat model. It is important to note that the requirements for a threat model are dependent upon the scope agreed and system components being reviewed. The checklist below is a broad overview.

| Step | Details | Justification |
| :--- | :----------------------------------------------: | :----------------------------------------: |
| 1.1  | Data flow diagram is prepared and reviewed  :white_check_mark:| Ensure there this a technical understanding of how data flows through the components |
| 1.2  | Assets, Controls and Threat Agents identified :white_check_mark:| Critical for understanding the architecture and low level technical control points |
| 2.1  | Ensure purpose and of each flow is understood :white_check_mark:| Justification and classification of the flow of data is understood                 |
| 2.2  | Ensudre data transfer&storage crypto understood :white_check_mark:| To ensure approved ciphers used for data in transit and storage |
| 2.3  | How is authentication and authorisation achieved? :white_check_mark:| Understnding how trust is achieved and IAM model is a critical understanding |
| 2.4 | Are mechanism for secrets stored for data movement? :white_check_mark:| For each flow understanding secrets management is required |
| 3.1| Are source code and code dependency scanning implemented :white_check_mark:| Securing build phase of the system |
| 3.2 | For cloud is IaC and security policy as code implemented :white_check_mark:| Securing cloud infrastructure built and implementing security policy |
| 3.3 | Are built artifacts dynamically scanned for weaknesses :white_check_mark:| Provides security assurance of what has been deployed is secure |
| 3.4 | Are built artifacts dynamically scanned for weaknesses :white_check_mark:| Provides security assurance of what has been deployed is secure |
| 4.1  | Application security reviewed against OWASP App Sec Verification Standard :white_check_mark:| Use of industry standard to validate application security posture |
| 4.2  | Infrastructure and cloud platform security reviewed against CIS benchmarks :white_check_mark:| Use of industry standard to validate infra and cloud security posture |
| 5    | Review what auditing and logging employed :white_check_mark:| Ensure security event information from systems is captured and alerted upon |
| 6 | If applicable review penetration test findings or conduct penetration test :white_check_mark:| Provide assurance across the system that exploitable vulnerabilities have been assessed|

### Tooling<a name="tooling"></a> 
There is no one specific silver bullet for tools to use for threat modelling. A number of tools are used, for example drawing tools and specific tools to map the attack surface and if required tools for penetration testing. A growing trend now is to use AI assisted (OpenAI GPT-3 model) tools, for example for subdomain discovery.

## About the author<a name="author"></a> 
I am cyber security practioner with over 20 years of experience working with a number of organisations as a security engineer and expert threat modeller. My background is as a trained chemist and applied physicist with a lifelong interest in science and the physical world.

After graduating I spent a number of years building and design security global networks and then time as an application security engineer.

The threat modelling methodology presented is as a consequence of experience securing and building production scale technical environments. My profile is on linked in [here](https://www.linkedin.com/in/haseeb-chaudhary-07695938/)
