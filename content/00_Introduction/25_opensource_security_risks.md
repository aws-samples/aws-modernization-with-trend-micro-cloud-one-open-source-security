---
title: "Open Source Security Risks"
chapter: false
weight: 25
---

### Manage Open Source Code Security Risks

Open source code is in the vast majority of commercial software today. Learn best practices to mitigate the unique risks that accompany its use.

The adoption of open source code has increased exponentially over the past decade, with a large percentage of commercial software now containing it. Developers are constantly sharing common features and code functionality across the internet and globe. The speed and demand placed upon application teams is high – business used to run via application releases a handful of times per year, and now is done a handful of times per week or day. This rapid acceleration pushed the world to move from “waterfall” and “iterative” project methodologies to “agile” to meet the rapidly growing demand.

Open source code comes from a myriad of sources. Code reuse, third-party libraries, and developer downloads tend to dominate the landscape. Also, realize the consultant that you are paying $250/hour to work on your project is using the same code they used for another client’s project last year. Reuse of code from one project to another is common—after all, if it work for Client X’s project, and Client Y is doing something similar, let’s re-use the code and save money:

![security](/images/open_source_security_risk.png)
**Image Source:** https://www.slideshare.net/denimgroup/create-a-unified-view-of-your-application-security-program-black-duck-hub-and-threadfix


For example, in the 2010’s, Capital One followed the waterfall methodology. The organization lives in the heavily regulated financial industry and is currently using open source as a part of their daily work. They’ve even built large components of their platform off it. In 2012, they were not open-source friendly with a “say no to open source” company mindset. Eventually, they realized they were using:

- Java (open source)
- Linux (open source)
- Apache (open source)
- Eclipse (open source)

They realized quickly they were building their environment off open source. Through a migration from commercial source code management to subversion and their own architecture, they were able to launch their production applications (built in-house) with open source code as part of the foundation. With specific processes put in place to mitigate the risks associated with open source code use, such as legal review, they were able to successfully execute without breaches or “secret” code releases.

 “Using open source software gives us numerous advantages from a business perspective. Open source gives us the ability to re-use what already exists and works well, with full flexibility to customize and/or contribute back what we need for our business. It also means that we are inherently building with technology that a broader community is investing in, dramatically reducing the likelihood that we are relying on end-of-life tech as well as making us more permeable to the larger talent ecosystem” – John Schmidt, Product Manager, Capital One

#### Open source isn’t completely free:

A common misconception of open source code is that it is free. Like a free puppy, it’s cute to have, but you still must care for it and feed it. To benefit from open source code use, you need to get the right people, and tech involved to mitigate for the unique risks associated with it.

#### Legal Open Source Risk:

- Licenses: Authors of software have rights to their code.
    - Permissive (giving credit) vs. copy left (distribute and show source code + share code being touched)
    - Using code is as-is (no recourse to the author)
    - Request changes or pull requests
- Trade secret disclosure (IP infringement)
- Devaluation of patent portfolio
- Merger and acquisition impact
- Reputational risk

In fact, many large companies such as Capital One and Facebook have open source legal counsel on staff. For example, during a merger and acquisition, they will advise on any open source issues during due diligence, and then after the acquisition they work in partnership with the integration team.

#### Open Source Security Risks:

- Vulnerabilities: Average of 64 vulnerabilities per code base and over 1500 days before a fix is available. Development processes are your first line of defense.
- You build it, you own it.
- Software of unknown origin.
- Continuous monitoring of configurations and environment.

To mitigate the risks, usage of open source repository scanning technologies is mandatory. A service which can find manifest files (identify and analyze), understand the direct and indirect dependencies, and flag them for known vulnerabilities is a must. Having integration into your code repository also helps identify your risks tied to your projects. Building the issue findings into your ticketing system (or creating pull requests) for remediation, at the developer level, is the next step to ensure the code has ownership and is cared for during its lifecycle. Maintenance and auditing (remediation) of this will be required because every time the same pull request happens, a scan and updated patch request must occur there too.

Building a culture among your organization to have ownership of code, the maintenance of it, and pride in the application from build to release will take time. Implementing the technology checks will assist in keeping the teams involved and more secure, as will doing this continuously.

#### 4 best practices to mitigate open source code vulnerabilities:

- Identify: Maintain open source inventory
- Analyze: Track open source vulnerabilities and licenses
- Remediate: Fix, patch, and upgrade
- Audit: Continuous monitoring

To help prevent the costly mistakes caused by open source vulnerabilities and license risks, SecOps teams can implement a solution like Trend Micro Cloud One – Open Source Security by Snyk. This helps secure open source inventories throughout the application development with increased visibility for earlier identification and continuous monitoring to minimize exposure over time.