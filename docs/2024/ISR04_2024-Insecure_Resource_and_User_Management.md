---
title: Insecure Resource and User Management
layout: col-sidebar
tags: owasp top-10 threats infrastructure infrastructure-threats security risks infrastructure-security-risks insecure resource and user management isr04
---

# ISR04:2024 – Insecure Resource and User Management

## Description
A big part and challenge of running an IT infrastructure is managing its resources and users.
Even more challenging is secure infrastructure.
It is mandatory to plan out the resources and access management, like who should have access to what and which user should have which permissions.
Questions like: What type of data needs to be stored where and how, must be asked and answered.
Most companies rely on centralized resource and user management tools like Active Directory or Microsoft Entra ID.
The management of these complex tools itself is challenging. Many vulnerabilities arise when these tools are rolled out without a proper security concept.
Besides that, permission and rights management are often neglected and users or technical users have more permissions than they actually need.

## Risk
Insecure Resource and User Management can lead to various security risks and vulnerabilities.
For example, having more permissions than needed increases the risk of giving threat actors more access once a user account is compromised, leading to a greater chance of devastating cyberattacks.
Additionally, rights and permissions might not be revoked, or user accounts aren't deleted after an employee left the company.
The accounts' security is at risk if regulations like password policies aren't enforced.
The same applies to resources like access to data or access to applications.
Because these resources and users can quickly add up, it is difficult to maintain a good overview, and risks arise over time.

## Rectification
To securely manage resources and users, different things are needed.
Foremost, it is recommended to develop a strategy, what resources are present and who needs access to them. The same applies to other kinds of permissions.
The need-to-know principle should always be kept in mind. Following the principle, the strategy and concept should be applied to the infrastructure and its technology, e.g. Active Directory.
Afterward, it needs to be ensured that restrictions apply, and the used tool is configured securely.
Additional tools, principles and concepts like Privileged Access Management - PAM should be implemented to harden the Resource and User Management.
Authorization Management - a small team that decides who gets which rights / permissions and for how long - should also be added.
Updating resources and a user's inventory is important, e.g. a new server is added, or an old one is resigned.

## Example Attack Scenarios
**Scenario #1: Insecure Privilege Management**
A company has a conventional infrastructure and different IT systems for managing their fabrication facilities.
It uses active directory for its resource and user management related to the IT infrastructure.
All employees have local administration rights allowing them to install additional software on their own devices.
Every administrator of the IT team has domain-admin rights, which they use to administrate the employee's device, help with problems, and manage the infrastructure.
One of the employees gets an email with a malicious attachment.
The employee is tricked into opening the attachment via social engineering methods used by a threat actor.
The employee's laptop is now infected without anyone knowing.
Because the employee's local admin rights, the threat actor is able to run an exploitation tool like mimikatz, which is able to extract credentials from the local system.
The system runs Windows, which stores user credentials for a specific time. One of the IT administrators logged on to the employee's laptop a few hours ago to help with a 
printer problem.
The credentials are still stored on the employee's local laptop, which the threat actor extracts using mimikatz and the local admin right.
This way, the threat actor easily compromised credentials for a domain-admin account.
Because domain admins are the highest privileged accounts in an active directory domain, the threat actor now has control over almost every component of the infrastructure and, therefore, compromised 
the whole infrastructure by attacking a single system.
The whole infrastructure and company got compromised by a threat actor due to the lack of secure resource and user management. There was no privileged user management 
following the need-to-know principle.

**Scenario #2: Deprecated and Insecure User Accounts**
A company has an internal infrastructure with a central customer data management system.
The company doesn't implement its password policy technically.
One employee works remotely and goes into a café to work from there.
They go to the toilet and leave their locked laptop on their table.
A threat actor uses this opportunity and goes to the laptop.
The threat actor tries a few standard passwords and manages to get access after a few tries.
They find a link to the central system managing the company's customer data.
They copy all the data to their phone using a cable they had in their backpack.
Afterward, they find an administrative share in the company's network holding sensitive configuration data, which they also extract.
Therefore, the threat actor was able to get access by abusing a weak password and also extracting not only data the employee typically accesses but additionally sensitive administrative data because no 
qualitative resource management and password policy was in place.

