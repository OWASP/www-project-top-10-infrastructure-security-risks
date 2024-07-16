---
title: Open Call for Data
layout: col-sidebar
tags: owasp top-10 insider-threats insider threats open call for data
---

# Open Call for Data -> OWASP Top 10 Insider Threats - Version 2026

## Motivation
To further improve the quality and significance of the OWASP Top 10 Insider Threats, we kindly invite you to join our Open Call for Data for 2024 and 2025. There, you can contribute data, anonymously or publicly, to the project. Throughout 2024 and 2025, we will collect all the data and then process this data for use in 2026. This way, we plan to publish the OWASP Top 10 Insider Threats - Version 2026 using an even more extensive dataset and further improve the quality and significance. If desired, contributors and donors will be recognized as sponsors on the relevant project pages. We also have plans to conduct CVE and CWE research for vulnerabilities regarding insider threats.

## What Data is needed?
We are looking for data regarding vulnerabilities in the context of insider threats e.g. findings from internal penetration tests or similar.
That way we can use the resulting dataset to evaluate what are the most common and critical vulnerabilities arising in internal IT-infrastructures.

## How to submit data?
To submit data, please prepare your data to fit to the following CSV structure and submit it as one CSV file.
The CSV can then be submitted via the linked Google Forms Document where you need to fill in additional data.

### Google Forms Document
[Google Forms for Data Submission](https://forms.gle/m4iTGL3baKZvzHAB7)

### CSV Structure

```text
id, count, [CWE], [INTXX:2023], (CVSS v3 score), (CVSS v3 vector), CVSS v4 score, CVSS v4 vector, title, description and details, (risk), (rectification) 
```

- Fields with no brackets are mandatory.
- Fields with [] brackets aren't mandatory but highly recommended, otherwise we might not be able to process and use your data.
- Fields with () brackets are optional and doesn't need to be filled out but would help us in the later stages of the analysis.

### Field Explanation

- id: Rolling identifier of finding.
- count: How many times this finding was found.
- \[CWE\]: If possible, relating CWE Number.
- \[INTXX:2023\]: If possible, relating number of OWASP Top 10 Insider Threats - Version 2023.
- CVSS v3 score: The CVSS v3 score of the finding.
- CVSS v3 vector: The CVSS v3 vector of the finding.
- CVSS v4 score: The CVSS v4 score of the finding.
- CVSS v4 vector: The CVSS v4 vector of the finding.
- title: The title of the finding.
- description and details: Brief description and explanation of the finding.
- (risk): Risks resulting from the finding.
- (rectification): How to rectify the finding.

### CSV Example

```text
id, count, [CWE], [INTXX:2023], (CVSS v3 score), (CVSS v3 vector), CVSS v4 score, CVSS v4 vector, title, description and details, (risk), (rectification) 

#1, 42, CWE-1104, INT01:2023, 10.0, CVSS:3.0/AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H, 10.0, CVSS:4.0/AV:N/AC:L/AT:N/PR:N/UI:N/VC:H/VI:H/VA:H/SC:H/SI:H/SA:H, Unsupported windows XP client with known vulnerabilities, A Windows XP Client was found. This version of Windows from Microsoft isn't supported anymore. There are no longer security patches and many publicly known exploits exists, including critical ones., Because this version of windows is no longer supported and there aren't security patches anymore, the number of known and critical exploits, without solutions to them, increases by time. These vulnerabilities can lead to the whole compromization of the system., It is recommended to upgrade the system to a up-to-date and supported version.
```

### Metadata

When you fill out the Google Forms Document, you will also be asked to enter additional information about yourself and your data.

Further explanation is stated in the Google Forms Document.

## Contact
If you have any questions regarding this process, feel free to write us an E-Mail:

[Nick Lorenz](mailto:nick.lorenz@owasp.org) and [Tim Barsch](mailto:tim.barsch@owasp.org)