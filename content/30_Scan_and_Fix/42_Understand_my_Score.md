---
title: "Understanding my Score"
chapter: false
weight: 42
pre: "<b>4.2 </b>"
---

## What is the Snyk Priority Score?

Snyk created a Priority Score to make the prioritization of issues as quick and easy as possible, ensuring the highest-risk issues have the highest score.

Scores are calculated and shown for all issues, vulnerabilities, and licenses. They range from 0 to 1,000 (0 is considered low risk and 1,000 is considered critical), giving users a high degree of granularity that reflects the many considerations taken into account. The granularity avoids having too many issues ending up with the same score, allowing users to determine priority quickly with a high degree of accuracy.

For each issue, Snyk processes and weighs several factors in a proprietary algorithm to produce the score for that issue. Currently, these factors include:

* Base severity: Uses Snyk's Severity levels and CVSS scores for that issue.
* Exploit Maturity: Determined by Snyk’s industry-leading security team using manual and automated methods to track which vulnerabilities are exploitable and to what extent.
* Reachability: By looking at the code paths called within a project, Snyk identifies which vulnerabilities are reachable from the code.
* Fixability: Without a safer version to upgrade to, or a Snyk patch available, developers must either fix the code themselves or use an alternative package. Vulnerabilities with fixes are given higher priorities.
* Time: New vulnerabilities are likely to be an increased risk, therefore increasing their priority score.


## How is a vulnerability’s severity determined?

Snyk uses the CVSS Framework v3.1 to communicate the characteristics and severity of vulnerabilities. A vulnerability's severity (critical, high, medium or low) is based on its CVSS score.


<table>
<tr>
 <th scope="col">Severity</th>
 <th scope="col">CVSS v3 Rating</th>
</tr>
<tr>
 <td>Critical</td>
 <td>9.0 - 10.0</td>
</tr>
<tr>
<td>High</td>
<td>7.0 - 8.9</td> 
 </tr>
<tr>
<td>Medium</td>
<td>4.0 - 6.9</td>
</tr>
<tr>
<td>Low</td> 
<td>0.1 - 3.9</td>
</tr>
</table>

The score is comprised of measurements of each of the following metrics:

* Attack Vector (AV)
* Attack Complexity (AC)
* Privileges Required (PR)
* User Interaction (UI)
* Scope (S)
* Confidentiality ( C)
* Integrity (I)
* Availability (A)