---
title: Insecure Use of Cryptography
layout: col-sidebar
tags: owasp top-10 threats infrastructure infrastructure-threats security risks infrastructure-security-risks insecure use of cryptography isr05
---

# ISR05:2024 – Insecure Use of Cryptography

## Description
Encryption plays an important role in cyber defense.
This is well-known for external applications and systems but is often overlooked regarding internal networks and infrastructures.
Companies and users have to keep in mind that if they don't implement sufficient encryption and cryptographic methods on their systems and protocols used in the internal network, an adjacent threat actor may be able to read, modify or inject data into communications and systems. This lack of encryption can lead to data leakage and the compromising of privileged accounts.
It is important to remember that a defense line only to the outside doesn't fully protect the internal systems. As soon as an attacker gains access to the internal network, e.g. via phishing, the outside defense line is mostly obsolete. That is why the security of internal infrastructures has to be as secure as an external system or even more.


## Risk
If insecure cryptographic methods or cryptographic configurations are used, the risk of information leakage and compromising (privileged) accounts is high.
This significantly raises the chances of a devastating cyberattack and its impact. For example, if an administrator connects to an internal server with a common remote access protocol like Remote Desktop Protocol - RDP and no encryption or an insecure one is configured, an adjacent and local threat actor can read these credentials from the network and easily compromise a privileged account.
The same applies to sensitive information send over the internal network. A company's internal infrastructure typically has many protocols, tools and systems to transfer data or access various components. Each must be configured to use sufficient and secure encryption / cryptographic methods to protect the data and accounts.


## Rectification
It is recommended to ensure all protocols, communications tools, remote access tools, data transfer tools and similar are configured to use secure cryptographic methods and configurations.
Additionally, protocols not supporting secure encryption should be migrated to a secure alternative, such as TELNET -> SSH and FTP -> SFTP.
Ensure the used cryptographic methods and configurations are sufficient, implement them after best practices and follow official recommendations.
Cryptographic functionality should not be developed or implemented by oneself; instead, use publicly available and known libraries, "Don't roll your own crypto!".


## Example Attack Scenarios
**Scenario #1: Unencrypted Remote Access Tools**
A company has a common internal it-infrastructure with different internal servers to provide applications to the employees. One of these applications is a Customer Relationship Management - CRM system which holds important and sensitive data about the customers of the company.
A threat actor gains access to the internal infrastructure over an unknown internet-exposed system for the company, which resulted from a misconfiguration.
The threat actor sniffs the internal network, listening to all internal network traffic from the machine they first compromised.
An administrator connects to an internal file server to perform an update and uses telnet to connect to the server.
Because telnet has no data encryption, the administrator's credentials are sent in clear text over the internal network.
The threat actor is able to capture this network packet and, therefore, compromises the administrator's account.
They use these credentials to log on to the CRM server and exfiltrate all the customer data they later sell to a concurrent company.

**Scenario #2: Insufficient Use of Cryptography**
A company has an internal IT infrastructure with several internal applications.
One of these applications is used to create invoices for company customers.
A threat actor gains access to the internal network and can inspect and inject packets into the internal network traffic.
An employee connects to the invoice system to create multiple invoices.
The communication protocol between the employee's laptop and the invoice server is encrypted but doesn't perform a cryptographic identity or integrity check.
The threat actor uses this vulnerability to perform a Man in the Middle - MitM attack and injects and modifies data packets.
The threat actor modifies the data the employee sends to the invoice server to redirect the money not to the company's account but to an account controlled by the threat actor.
When the customer pays the invoice sent to them, they transfer the money to the attacker instead of the company.
