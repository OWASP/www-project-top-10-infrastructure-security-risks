---
title: Insecure Authentication Methods and Default Credentials
layout: col-sidebar
tags:
  - owasp
  - top-10
  - threats
  - int07
  - insecure
  - and
  - default
  - credentials
  - infrastructure
  - infrastructure-threats
  - authentication
  - methods
---

# INT07:2024 – Insecure Authentication Methods and Default Credentials

## Description
Passwords are still a fundamental part of cybersecurity, and many Identity and Access Management (IAM) Systems rely on username and password authentication. Insecure Authentication Methods are a common vulnerability in cybersecurity, referring to passwords that are easy to guess or crack due to their simplicity, predictability, or lack of complexity (length). Default credentials preconfigured on hardware devices or software applications by manufacturers or vendors are often left unchanged by users or administrators, creating a security vulnerability.

## Risk
Credentials are crucial to provide only authenticated and authorized users access to internal resources. Weak passwords can be easily exploited through various techniques, such as brute-force and dictionary attacks. Default credentials, however, can effortlessly be found in the documentation of the used product. Attackers can exploit devices or applications with unchanged default settings or stolen passwords. This can lead to unauthorized access, data breaches, and the compromise of critical systems.

## Rectification
Organizations should enforce password complexity requirements to mitigate the risk, implement multi-factor authentication (MFA), and educate employees about the importance of strong, unique passwords. Password management tools can also help enhance security.

## Example Attack Scenarios
**Scenario #1: Printer**
Many networked printers are shipped with default usernames and passwords that are widely known. An attacker could exploit this by accessing the printer and viewing printing jobs containing sensitive information. To prevent this, organizations must change default printer credentials upon installation and restrict access to authorized personnel.

**Scenario #2: User Accounts**
Weak or easily guessable passwords for user accounts are a primary target for attackers. In an attack scenario, a malicious employee could gain unauthorized access to sensitive information or systems by exploiting weak user passwords. To counter this threat, organizations should enforce password policies, implement account lockouts after multiple failed login attempts, and promote password best practices among users.

