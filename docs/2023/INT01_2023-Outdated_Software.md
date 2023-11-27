---
title: Outdated Software
layout: col-sidebar
tags: owasp top-10 insider-threats insider threats int01 outdated software
---

# INT01:2023 – Outdated Software

## Description
It is important to keep software updated.
Often, updates include security-relevant patches, meaning if a software isn't up-to-date, it may contain vulnerabilities in its current version state.
These vulnerabilities are often publicly known and can be found easily by security scanners.
Unfortunately, many companies and end users fail to keep all their software components up-to-date.
Due to the lack of updates and update management, many software components and underlying systems become vulnerable over time, with increasing criticality as time passes by.

## Risk
Outdated software can lead to a variety of different vulnerabilities, ranging from vulnerabilities with a low criticality to vulnerabilities causing compromization of the entire system.
The severity and amount of these vulnerabilities in an outdated software system depends on the individual case.
Usually, they rise with time as more and more vulnerabilities are found.

## Rectification
It is recommended to keep all software components, including libraries and similar, on an up-to-date, stable and supported version.
Every software and its components should be regularly checked for updates and new patches.
It is recommended to implement an update management process to ensure no components are missed, and the checks are in time.
It makes sense to regularly check vendor sites and information security hubs for news about zero-day exploits for related software.
In this case, there might be no updates to these kinds of vulnerabilities, but the company or individual can take precautions to reduce the impact or the probability of these vulnerabilities.

## Example Attack Scenarios
**Scenario #1: Outdated Web Server**
A company hosts an internal website to provide information to its employees.
The company doesn't have an update management process and doesn't regularly check and update its software components.
The web server used for this website runs on an outdated version with known vulnerabilities. One of these vulnerabilities is a Remote Code Execution - RCE.
An attacker who gained access to an employee's computer enumerates the version of the internal web server and quickly finds a related Common Vulnerabilities and Exposures - CVE for the current web server version regarding a 
Remote Code Execution.
The attacker manages to find a related exploit and gains access to the underlying server.

**Scenario #2: Deprecated Old Server**
A company has an update management process to keep all its software components up-to-date.
The update management process failed to inventory an old internal server with confidential construction plans.
An attacker who gained access to the internal company's network finds this server and enumerates its OS version.
The attacker finds out the vendor no longer supports the used version and is prone to several vulnerabilities, including critical ones.
The attacker uses a publicly available exploit to access the server and exfiltrates the confidential construction plans, selling them to company competitors afterward.
