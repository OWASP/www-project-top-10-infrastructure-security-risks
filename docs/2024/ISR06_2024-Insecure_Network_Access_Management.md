---
title: Insecure Network Access Management
layout: col-sidebar
tags: owasp top-10 threats infrastructure infrastructure-threats security risks infrastructure-security-risks insecure network access management isr06
---

# ISR06:2024 – Insecure Network Access Management

## Description

Network Access Management is a fundamental aspect of the architecture of internal infrastructures and the access control regulations.
A qualitative Network Access Management prevents a variety of attacks and can reduce the impact of cyberattacks as well as the movement of threat actors inside the internal infrastructure.
A more critical and severe risk is the lack of network separation, which would restrict access from one part of the internal infrastructure to others.
Often, companies don't prevent threat actors from accessing the internal network if the attacker manages to get physical access to a network port or Wi-Fi nearby.
Additionally, traffic should be supervised and regulated context-based closely to the application layers for communication paths that need to be allowed.

## Risk

The absence of network separation will severely increase the risk of cyberattacks spreading through the internal infrastructure and, therefore, increase the risk of the compromization of the
whole infrastructure, even though only one component was compromised.
If no network access control is in place, an attacker is able to get access to internal networks if the threat actor manages to gain physical access to network components, gets employees to
plug in malicious devices or gets access to a nearby Wi-Fi.
Insufficient access regulations to components of the infrastructure or, to be more precise, network regulations closer to the application layers can allow threat actors to abuse commonly allowed
communication paths.

## Rectification

It is recommended to implement Network Access Control - NAC mechanisms as part of the Network Access Management.
These technical regulations, e.g. certificate-based NAC, will ensure that only approved devices can access the company's network.
Ideally, network separation should be taken into account in the architecture phase of an infrastructure. Similar to the need-to-know principle, network chunks should be kept as small as possible as
well as the number of communication paths between these chunks.
Technologies like Virtual Local Area Networks - VLANs can help to separate the infrastructure qualitatively.
An access matrix can assist in planning out the network access management structure.
The next recommended step is to supervise and regulate the communication paths between the "isolated" network chunks.
These bridges or network transitions should be dynamically regulated. Based on the application layer context, access to these subnetworks or components should be allowed or disallowed.
Remote access to the network, e.g. allowing employees to work from home, should be done securely using technologies like Virtual Private Networks - VPNs.

## Example Attack Scenarios

**Scenario #1: Insufficient Network Separation**
A company has an internal network infrastructure hosting different applications for its customers.
These applications can be accessed online so customers can use the services remotely.
The company has multiple database servers holding the data for the named application servers as well as servers for internal applications and data.
A threat actor finds a technical vulnerability in one of the publicly accessible application servers and gains complete control of the server.
Because of the lack of network separation, the attacker is able to easily move laterally and compromises all the database servers as well as the internal application and data servers.
The threat actor compromises the internal infrastructure, pivoting from only one initial access point.
Later, the exfiltrated data is sold to other cybercriminals.

**Scenario #2: Deprecated Old Server**
A company uses a common internal infrastructure with application servers and employee file shares.
The company orders new network printers to replace their old ones.
A threat actor is able to inject malicious hardware into the new network printer before it arrives at the company.
When the new network printers are plugged into the internal network, the malicious hardware, consisting of a small computer, also uses the network port to get access to the internal network and
isn't blocked because no NAC is in place.
It then connects to a remote host via the internet controlled by the threat actor, who establishes a connection back and creates a pivot point into the internal network from where additional attacks
can be performed.
