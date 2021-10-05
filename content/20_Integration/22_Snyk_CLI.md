---
title: "Snyk CLI"
chapter: false
weight: 33
pre: "<b>3.3 </b>"
---

### What is the Snyk CLI on Trend Micro Cloud One - Open Source Security by Snyk?

Snyk CLI (Command Line Interface) allows you to find and fix known vulnerabilities in dependencies, both manually and as part of your continuous integration (CI) workflow, in a command line environment.

See [Language Support](https://support.snyk.io/hc/en-us/articles/360020352437-Language-support-summary) for details about package managers and languages. 

---

#### Prerequisites

- Install the Snyk CLI: [**Link**](https://support.snyk.io/hc/en-us/articles/360003812538-Install-the-Snyk-CLI)
- Check if you have Git installed in your machine. If not, here is the [**link**](https://github.com/git-guides/install-git) 


{{% notice warning %}}
**Make sure you have the above requirements deployed in your machine. If not, it won’t work properly based on this lab for the Snyk CLI.**
{{% /notice %}}


---

### Getting Started with the Lab

During this lab with the Snyk CLI, we will use the [**Goof**](https://github.com/snyk/goof) application, which is available on Snyk GitHub. The vulnerabilities and licenses risks will be shown inside the **Trend Micro Cloud One - Open Source Security by Snyk** dashboard. 

#### 1. Open the [Trend Micro Cloud One console](https://cloudone.trendmicro.com/), select the Open Source Security by Snyk tile, and then click on Head to Snyk.
![SnykCLI](/images/snyk_cli_1.png)

![SnykCLI](/images/snyk_cli_2.png)

![SnykCLI](/images/snyk_cli_3.png)

#### 2. Click on Integrations and select CLI tile under Continuous integration:
![SnykCLI](/images/snyk_cli_4.png)

#### 3. Scan your code locally

![SnykCLI](/images/snyk_cli_5.png)

- **Install the Snyk tool if you haven’t yet.**

{{% notice tip %}}
Make sure you have homebrew if you are using the command above. If not, you will need to install it on your machine. Here is the [link](https://brew.sh/)
{{% /notice %}}

{{% notice note %}}
Check the description of a different command if you are using a different operation system.
{{% /notice %}}

---
### **Mac or Linux example**

<details>
  <summary> -> <code>CLICK HERE</code> to see Mac and Linux example to install Snyk tool</summary>

Command for Mac or Linux: ```brew tap snyk/tap```

        $ brew tap snyk/tap
        Updating Homebrew...
        ==> Auto-updated Homebrew!
        Updated 1 tap (homebrew/core).
        ==> New Formulae
        fanyi
        ==> Updated Formulae
        Updated 46 formulae.

        ==> Tapping snyk/tap
        Cloning into '/usr/local/Homebrew/Library/Taps/snyk/homebrew-tap'...
        remote: Enumerating objects: 1564, done.
        remote: Counting objects: 100% (528/528), done.
        remote: Compressing objects: 100% (402/402), done.
        remote: Total 1564 (delta 170), reused 471 (delta 124), pack-reused 1036
        Receiving objects: 100% (1564/1564), 205.94 KiB | 1.11 MiB/s, done.
        Resolving deltas: 100% (658/658), done.
        Tapped 1 formula (19 files, 258.5KB).

Command for Mac or Linux: ```brew install snyk```

        $ sudo chown -R $(whoami) /usr/local/share/man/man8
        $ brew install snyk                           
        ==> Installing snyk from snyk/tap
        ==> Downloading https://static.snyk.io/cli/v1.675.0/snyk-macos
        ######################################################################## 100.0%
        Warning: A newer Command Line Tools release is available.
        Update them from Software Update in System Preferences or run:
        softwareupdate --all --install --force

        If that doesn't show you any updates, run:
        sudo rm -rf /Library/Developer/CommandLineTools
        sudo xcode-select --install

        Alternatively, manually download them from:
        https://developer.apple.com/download/more/.
        You should download the Command Line Tools for Xcode 12.5.

        🍺  /usr/local/Cellar/snyk/1.675.0: 3 files, 46.0MB, built in 5 seconds
        ==> `brew cleanup` has not been run in 30 days, running now...
        Removing: /Users/fernandoca/Library/Caches/Homebrew/hugo--0.83.1... (35MB)
        Removing: /Users/fernandoca/Library/Logs/Homebrew/hugo... (64B)

</details>
---

---


### Windows Example 

<details>
  <summary> -> <code>CLICK HERE</code> to see Windows example to install Snyk tool</summary>

Powershell :laptop:

**Command:** Set-ExecutionPolicy RemoteSigned -scope CurrentUser


        PS C:\Users\Administrator> Set-ExecutionPolicy RemoteSigned -scope CurrentUser

        Execution Policy Change
        The execution policy helps protect you from scripts that you do not trust. Changing the execution policy might expose
        you to the security risks described in the about_Execution_Policies help topic at
        https:/go.microsoft.com/fwlink/?LinkID=135170. Do you want to change the execution policy?
        [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y


**Command:** Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')

        PS C:\Users\Administrator> Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
        Initializing...
        Downloading scoop...
        Extracting...
        Creating shim...
        Downloading main bucket...
        Extracting...
        Adding ~\scoop\shims to your path.
        'lastupdate' has been set to '2021-08-12T11:38:28.7910987+00:00'
        Scoop was installed successfully!
        Type 'scoop help' for instructions.

        
**Command:** scoop bucket add snyk https://github.com/snyk/scoop-snyk

        PS C:\Users\Administrator> scoop bucket add snyk https://github.com/snyk/scoop-snyk
        Checking repo... ok
        The snyk bucket was added successfully.
  
        
**Command:** scoop install snyk

        PS C:\Users\Administrator> scoop install snyk
        Installing 'snyk' (v1.679.0) [64bit]
        snyk-win.exe (46.3 MB) [======================================================================================] 100%
        Checking hash of snyk-win.exe ... ok.
        Linking ~\scoop\apps\snyk\current => ~\scoop\apps\snyk\v1.679.0
        Creating shim for 'snyk'.
        'snyk' (v1.679.0) was installed successfully!    

</details>
---

---

#### In your terminal, clone the Goof repository for your machine

Command: ```git clone https://github.com/snyk/goof.git```

        $ git clone https://github.com/snyk/goof.git
        Cloning into 'goof'...
        remote: Enumerating objects: 2201, done.
        remote: Counting objects: 100% (39/39), done.
        remote: Compressing objects: 100% (39/39), done.
        remote: Total 2201 (delta 21), reused 6 (delta 0), pack-reused 2162
        Receiving objects: 100% (2201/2201), 4.66 MiB | 10.27 MiB/s, done.
        Resolving deltas: 100% (1489/1489), done.

Nagigate into the goof folder from the application 

Command: ```cd goof/```

        $ cd goof/

--- 

**Authenticate your machine with Trend Micro Cloud One - Open Source Security by Snyk**

Command: ```snyk auth```

        $ snyk auth

        Now redirecting you to our auth page, go ahead and log in,
        and once the auth is complete, return to this prompt and you'll
        be ready to start using snyk.

        If you can't wait use this url:
        {TOKEN URL to copy and access in your brower or you may be automatically redirect}

        \ Waiting...


- The authentication page should automatically open. If it doesn’t, copy the URL with the TOKEN generated into the CLI and paste it into your browser with the opened Trend Micro Cloud One console. This ensures that the Trend Micro Cloud One session is automatically used to authenticate with Snyk CLI.

![SnykCLI](/images/snyk_cli_6.png)

![SnykCLI](/images/snyk_cli_7.png)

---

- **Analyze and test your dependencies**

Return to the terminal and run the command **snyk monitor** from the Snyk CLI:

Command: ```snyk monitor```

        $ snyk monitor                                  

        Monitoring /Users/fernandoca/Documents/VirtualEnv/goof (goof)...

        Explore this snapshot at https://app.snyk.io/org/trend-micro-<API>
    
        Notifications about newly disclosed issues related to these dependencies will be emailed to you.

--- 

{{% notice tip %}}
If you receive the following error **Authentication failed. Please check the API token on https://snyk.io** during the authentication process, try to add your Auth Token from Trend Micro Cloud One console in front of the **snyk auth API**
{{% /notice %}}

![SnykCLI](/images/snyk_cli_8.png)

---

Return to the Trend Micro Cloud One - Open Source Security by Snyk console and you will be able to see the Java Goof Application. Click on the Java Goof app to see more details.

![SnykCLI](/images/snyk_cli_9.png)


Now you can start investigating the vulnerabilities found using the Snyk CLI :laptop:

![SnykCLI](/images/snyk_cli_10.png)