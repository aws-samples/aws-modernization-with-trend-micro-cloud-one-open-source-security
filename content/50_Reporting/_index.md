---
title: "Reporting"
chapter: false
weight: 75
pre: "<b>5. </b>"
---

## How Can Security Teams use the Vulnerability and License Report?

Trend Micro Cloud One – Open Source Security by Snyk reporting provides security teams with an accumulated view of all issues across all your projects.

{{% notice tip %}}
**VALUE:** The Reports section displays historical and aggregated data about projects, issues, dependencies, and licenses. 
{{% /notice %}}

![Integration](/images/report1.png)

----

## Summary tab
The Summary tab provides AppSec teams with visibility into security issues by severity, license issues by severity, and issues over time. The Exposure Window shows elapsed time from when an issue was identified and until it was resolved. The Summary tab also displays activity including test runs, number of projects, new issues, fixed issues, tests preventing issues, and ignored issues.

{{% notice tip %}}
**VALUE:** The main dashboard displays a birds-eye view of all your issues (vulnerabilities and licenses), across all your projects.
{{% /notice %}}

Because your repository was loaded for this workshop, the Issues over time graph and Exposure window graph will not appear as extensive as the example below. The issues over time will adjust based on remediation of existing issues, and new issues arising.

![Integration](/images/report2.png)

{{% notice note %}}
For more details on the dashboard summary view, please visit [Snyk portal](https://support.snyk.io/hc/en-us/articles/360004002578-Summary-tab)
{{% /notice %}}

----

## Issues Tab
The Issues tab displays all known vulnerability and license discrepancies across your projects with details about each issue, possible remediation steps, and what projects are affected. 

{{% notice tip %}}
**VALUE:** All issues (vulnerabilities and licenses) across all your projects, including their severity, available remediation if any exists, and more.
{{% /notice %}}

- Click on the **Issues Tab**
- Click on the Projects filter
- Select the check box for **java-goof:todolist-web-struts/pom.xml**

![Integration](/images/report3.png)

Issues can be grouped or ungrouped based on the desired view and required details. Grouping the issues shows an aggregated view and rolls up the number of projects affected. Ungrouping the view shows a record for each project and more columns, including fixable, introduced, status, reachability, and Jira issue, if applicable.

For more details on the Issues tab please visit [Snyk portal](https://support.snyk.io/hc/en-us/articles/360004002598-Issues-tab)

- Click on the Issues Filter
- Select the following options to narrow down your search for specific priority scores and vulnerabilities to check on.

![Integration](/images/report4.png)

From the filtered list, that is now filtered, click on the Issue: Remote Code Execution (RCE) link to read more about this vulnerability and how to remediate it.

![Integration](/images/report5.png)

Return to the Issues tab using the back button on your browser menu. 

Now click on the **Dependencies tab.**

---

## Dependency Tab

The Dependencies tab acts as a Bill of Materials for all the dependencies in your projects. 

{{% notice tip %}}
**VALUE:** The dependency tab provides dependency health for your packages and displays details such as name, version, and which projects currently use the package. The report also gives transitive dependencies and helps identify healthy and deprecated packages.
{{% /notice %}}

- Click on the **Dependencies Tab**
- Filter on **Projects** for **/java-goof:todolist-web-struts/pom.xml** to see the following details:

![Integration](/images/report6.png)

For more details on the Dependency tab please visit [Snyk portal](https://support.snyk.io/hc/en-us/articles/360004002618-Dependencies-tab)

---

## Licenses Tab

The Licenses tab displays all licenses used in your project and a summary of all your projects’ dependencies. 

- Click on the **Licenses Tab**
- Filter on **Projects** for **/java-goof:todolist-web-struts/pom.xml** to see the following details:


![Integration](/images/report7.png)

1. **Search for Licenses**: The dynamic search field enables you to enter free text and begins searching with the first character you type. Alternatively, select multiple packages from the dropdown list. Click the Select All or Deselect All links that dynamically appear in the upper right-hand corner of the dropdown list.
2. **License filters**: Mark the packages you want to see by selecting specific project types. Only issues matching all selected criteria are displayed.

