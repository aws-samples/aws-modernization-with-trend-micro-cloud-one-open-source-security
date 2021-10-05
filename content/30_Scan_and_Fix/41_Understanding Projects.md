---
title: "Understanding the Projects"
chapter: false
weight: 41
pre: "<b>4.1 </b>"
---

### Dashboard Visibility for Your Projects

Trend Micro Cloud One – Open Source Security by Snyk consolidates all of your application projects and repos you want to monitor into one list for easy access and management. This dashboard gives a brief overview of the vulnerable packages, current security issues, and current license issues.

![Integration](/images/dashboard_visibility.png)

---

### Understanding Open Source Vulnerabilities in Your Projects

In Trend Micro Cloud One - Open Source Security by Snyk, information is organized based on projects. A project represents a manifest of listed open source components that a developer is using within an application. An example file might be ‘package.json’ or ‘pom.xml’. 

The open source components are tested by Trend Micro Cloud One – Open Source Security by Snyk to determine if any of open source libraries have vulnerabilities or license risks. Issues are determined by analyzing the package manager of your application and reviewing the direct and indirect dependencies. When developers create an application, they list the direct dependencies needed for the application to work and those dependencies have their own indirect dependencies. 

Let’s explore the Projects page. Click on the tab Project in the top menu bar.

![Integration](/images/projects1.png)

Projects are grouped in the UI based on the integration used to import the project. For example, if the project comes from GitHub, the UI will group all projects in the GitHub repo and display the total issues discovered. If the repo contains multiple package manager files in a single repo, often called a monorepo, all projects will be listed under the GitHub repo in the UI. 

Importing projects can be completed using various methods. The two most common are using the Snyk UI or the Snyk CLI. Snyk users can use the Snyk UI to import their projects by selecting the integration from the list of configured integrations.

![Integration](/images/projects2.png)

Above is an example of a GitHub repo with many project files, including the package manager for the source code pom.xml based on the source code in the repo.

Reviewing a project issues in the UI easy. Start by selecting the java-goof-trend project from the Projects tab.

Note: You can tag and label your projects to identify, aggregate, and search for them based on their 
key attributes.

- Click on todolist-web-struts/ pom.xml

![Integration](/images/projects3.png)

---

### Viewing Project Cards and Filters in the UI

An issue is either a vulnerability in the open-source dependencies or a dependency that violates the organization’s license compliance policy. Trend Micro Cloud One – Open Source Security by Snyk categorizes issues by severity, exploit maturity, status, and, most importantly, priority score. Each issue has a severity score based on CVSS v3.1 scoring. We will dive more into this shortly.

The issue displays the vulnerable module, how it was introduced, a detailed path, remediation advice, and in some cases, a descriptive overview. Finally, Trend Micro Cloud One – Open Source Security by Snyk provides a priority score to help security and development teams understand and prioritize the most critical issues to remediate.

![Integration](/images/projects4.png)

Let’s explore the filters: it is important to be able to make informed decisions on the types and severity of open source risk that could be impacting your projects. Here are some ways to zero in on specifics and gain new insights.

From within the todolist-web-struts/pom.xml package:

**1.**	We want to first look at **code injection** issues, so we will focus on CWE-94. Type CWE-94 in the search bar.

**2.**	On the left side panel select Vulnerabilities under Issue Type. Not all vulnerabilities are created equal, many have no known way of being exploited. As such, we want to target the ones that represent the greatest risk. For example, mature vulnerabilities have documented tools or procedures for allowing exploitation.

**3.**	Select Mature under Exploit Maturity

You should now have filtered the list down to two results.

![Integration](/images/projects5.png)

**4.**	Select Proof of Concept from the Exploit Maturity filter. Proof of Concept indicates that although there is no purpose-built code or tool for exploiting the given vulnerability, it has been proven that it could be exploited, which means there could be a tool developed and shared soon.

![Integration](/images/projects6.png)

**5.**	Looking at the upper part of the user screen, in the header filters, select **TAGS** and type in **Application**. Hit enter, then after insert the key **"todo"** and press enter again.

**6.**	Next, type Application, hit enter, and after insert the key **"Struts2-core"** and press enter again. It will look like the example below:

{{% notice note %}}
A tag is a key and value combination, which allows you to add additional custom metadata to projects.
{{% /notice %}}

![Integration](/images/projects7.png)


**7.**	Click on Environment, then select Frontend and External. This provides additional information that the risks in question are part of an external application and attributed to the frontend UI of the application.

**8.**	Under Business Criticality, select Medium.

**9.**	Under Lifecyle Stage, select Production.

![Integration](/images/projects8.png)

**10.**	From the top menu bar, click on Projects, this will open a new filter view on the left side of the page. 

![Integration](/images/projects9.png)

**11.**	On left side, select from the Tags menu Applications and after Todo. This narrows down your focus to a particular package out of the hundreds of projects that might be represented within the view for a single enterprise application.

![Integration](/images/project10.png)

**12.**	Select Production from the Lifecyle Menu. Although in our workshop you will only see one result, the value here is to focus on the vulnerabilities that are exposed immediately in production, this is another step in the triage process for DevOps and SecOps teams.

![Integration](/images/projects11.png)

Project attributes are static and non-configurable fields which allow you to add additional metadata (also known as “values”) to a project. Attributes have a predefined list of values you can select from.

Now that you learned how to get more insights from your projects it's time to understand a little bit more about the scoring inside Trend Micro Cloud One - Open Source Security by Snyk. Let's do it :laptop: :rocket:.