---
title: Insufficient Threat Detection
layout: col-sidebar
tags:
  - owasp
  - top-10
  - threats
  - int02
  - insufficient
  - threat
  - detection
  - infrastructure
  - infrastructure-threats
---

# INT02:2024 – Insufficient Threat Detection

## Description
Threat Detection plays a vital role in cyber defense.
In most Cyberattacks, especially internal ones, the first detection of threat actors is too late.
Most Cyberattacks get detected once the threat actors perform malicious actions that impact and disturb internal processes or interfere with employee's work.
For example, when ransomware starts to encrypt data on an employee's computer or an important server.
Unfortunately, a detection of a cyberattack in this state is too late.
Qualitative threat detection is needed to detect threat actors and malicious activities before they can cause severe damage.
Ideally, threat actors should be detected in the initial access phase or, at the latest, in the command and conquer phase.

## Risk
If threat actors aren't detected early on in a cyberattack chances are high that the target is powerless and doesn't get the opportunity to take further defense actions.
Threat actors are normally weeks and month in an internal network before they perform conspicuous actions.
Insufficient threat detection is one of the main reasons sophisticated cyberattacks are successful that often.
Without proper detection and monitoring mechanisms in place the target won't be able to see threat actors get access to their internal network and move laterally through it.

## Rectification
Implementing processes and mechanisms on different levels and points of the internal infrastructure is recommended to build a qualitative and powerful threat detection system.
Security Incident and Event Management - SIEM Systems, Firewalls, Endpoint Detection and Response - EDR Applications and other mechanisms and software that supervise activities, build 
the foundation of a threat detection system.
It is crucial to implement these sensors and systems on as many levels and points of the infrastructure as possible, like computers, servers, or the network on 
different ISO/OSI-Layers.
This way, the chances of early detection of cyberattacks and their threat actor are high. The target can take further actions and can defend the internal infrastructure before 
devastating attacks can be performed.

## Example Attack Scenarios
**Scenario #1: Insufficient Network Detection**
A company has an internal infrastructure, including endpoint systems, like employee computers, and servers for internal applications.
The internal servers hold mandatory data for the company's business processes. An End Point Detection and Response Software on every employee's device is implemented.
An employee accidentally downloads and executes malware without realizing it is malicious software.
An Advanced Persistent Threat - APT, a sophisticated and highly professionalized cybercriminal group, wrote the malware and the EDR fails to detect the malware.
The malware is able to compromise one of the internal servers from the compromised employee's computer. The malware moves laterally through the network and compromises all the 
internal servers. These actions aren't detected because no qualitative threat detection system exists for the network.
After compromization, the malware encrypts all data on the servers, the company loses access to its data and, therefore, can't keep its business processes running.
This could have been prevented if the company had implemented a redundant and complete threat detection and monitoring system and not only an EDR system.

**Scenario #2: Insufficient Anomaly Detection**
A company hosts internal services for employees to share critical data and files. It also provides the employees with laptops and configured Virtual Private Network - VPN software so that they 
can work from home.
An employee's laptop gets stolen on a train ride by a cybercriminal who manages to get access to the laptop and the employee's account.
The cybercriminal finds the internal shares and downloads the files from all shares. 
The company fails to detect this data exfiltration because it doesn't have an anomaly detection. It would have noticed the large transfer of data or the access to shares the employee 
typically doesn't access.
The cybercriminal later sells the exfiltrated data and files to concurrent companies.
