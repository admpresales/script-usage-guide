# script-usage-guide
This document lists demo assets that the field has found useful as part of a core demo or tailored demo.

**Most** of these test scripts are not considered part of the "core" demo assets which means you will **not** find them delivered as part of the [devops.dockerapp](https://hub.docker.com/r/admpresales/devops.dockerapp/) or the [devops](https://hub.docker.com/r/admpresales/devops/) images.  Test scripts that are shown on this page that **are** part of the core scripts delivered in the Devops image are noted with '(c)'.  For example:
```
uftdev-gherkin (c)
```

Instructions on [How to add a test script to devops container](#how-to-add-a-test-script-to-devops-container) can be found below. Alternatively, you could just clone or fork the repository into the file system of NimbusClient or NimbusServer.  

Instruction and expectations for those developing new test scripts can be found below:<br>
[Expectations for those developing new scripts](#Expectations-for-those-developing-new-scripts)

Almost all scripts are available on github, from the admpresales account. However, there are a few scripts that are availalble from other github accounts.
# R&D Assets.
R&D runs a suite of scripts nightly, as a part of their devops implementation. They are all LeanFT scripts, and are available here:
[R&D LeanFT Scripts](#https://github.com/aosapp/account-service).
These scripts are, in general, longer and more involved than those in the admpresales account, since they are trully used in a production environment, (as opposed to the scripts in admpresales, that are more demo focused). One way that this is apparent if you look at the details, is that these assets ONLY use objects in Application Models, so the Application Models are much more extensive than the ones in admpresales.

The details of the contents is contained in the project [README.md](https://github.com/aosapp/account-service/blob/master/README.md).
# admpresales Assets
## UFT One / UFT Developer Scripts <br>(prior to 2020, were LeanFT / UFT Developer)

| Script Name (now)                        | Name (pre 2020)                    | Note                                     |
|------------------------------------------|------------------------------------|------------------------------------------|
| [uftdev-aos-web-gherkin](https://github.com/admpresales/uftdev-aos-web-gherkin)<br>(c) | leanft-gherkin                     | IntelliJ - maven project which uses UFT Developer and gherkins features and files and cucumber for execution.  This one actually executes a test against AOS |
| [octane-gherkin](https://github.com/admpresales/octane-gherkin)<br>(c) | octane-gherkin                     | Very similar to UFT Developer_Gherkins with the exception that the Gherkin step definitions are left empty so it runs faster.  The intent here is to use when focusing on Octane demos only and UFT Developer is not a focus. |
| [uftdev-aos-web-se](https://github.com/admpresales/aos-web-lft4se) | aos-web-lft4se                     | Maven project demonstrating using UFT Developer for Selenium in a simple project.  This was created using the Selenium OIC. |
| [uftdev-se](https://github.com/admpresales/simple-lft-selenium) | simple-lft-selenium                | Simple script demonstrating Selenium and UFT Developer used together.  With webdriver launching and UFT Developer attaching to browser and using the Verify and Reporter classes |
| [oscillating](https://github.com/admpresales/oscillating) | oscillating                        | This script was used as part of a training session to demonstrate how areas of the Octane Pipeline Analysis screen gets populated based on how scripts run, pass, fail, etc. |
| [uftdev-aos-mobile-android](https://github.com/panama69/Mobile_AOS_Test) | Mobile_AOS_Test - Android          | Simple UFT Developer test against AOS on an Android device |
| [uftdev-aos-mobile-ios](https://github.com/admpresales/aos-ios-leanft) | Mobile AOS Test  - iOS             | UFT Developer tests against AOS on an iOS device |
| [uftdev-applitools](https://github.com/panama69/LeanFT_AppliTools) | LeanFT_AppliTools                  | Very simple UFT Developer/AppliTools test using C#.  The code came from AppliTools website but I added information to the readme to aid in setting things up |
| [uftdev-mobile-cross-browser](https://github.com/panama69/LeanFT_Cross_Browser_Mobile) | LeanFT_Cross_Browser Mobile | Simple script showing execution across the desktop Firefox browser and the iPhone Safari browser. |
| [testng-example](https://github.com/admpresales/testng-example) | testng-example                     | Simple TestNG tests using UFT Developer Reports to demonstrate how to run TestNG in parallel and pass arguments to a test |
## UFT One Scripts
| Script Name (now)                        | Name (pre 2020)                          | Note                                     |
|------------------------------------------|------------------------------------------|------------------------------------------|
| [uftone-gui-aos-order-purchase](https://github.com/admpresales/uft-gui-aos-order-purchase) | uft-gui-aos-order-purchase               | Demonstrates the shopping business process against AOS. The script logs into AOS; shops and completes the purchase (looping from a local data tabe) ; logs out |
| [uftone-flight-api-with-gui-verification](https://github.com/admpresales/flight_api_with_gui_verification) | flight-api-with-gui-verification         | Demonstrates using API test interacting (calling) GUI test.  This script is great for showing customer the value of using API testing with their regression suites. Much of regression testing is setting up specific data scenarios so users can perform the actual test they need. Using API for the setup can drastically reduce the overall execution time. |
| [uftone-flight-gui-comprehensive](https://github.com/admpresales/comprehensive-uft-test-flightgui) | comprehensive-uft-test-flightgui         | UFTOne script demonstrating several capabilites of UFT (courtesy Ron Sercely) |
| [uftone-aos-web-create-account](https://github.com/admpresales/uft-create-aos-account.git) | uft-gui-create-aos-account               | This UFTOne script which creates a new account in AOS |
| [uftone-using-an-Excel-sheet-with-more-than-256-columns](https://github.com/admpresales/UFT-using-an-Excel-sheet-with-more-than-256-columns.git) | UFT-using-an-Excel-sheet-with-more-than-256-columns | Prior to v15, The datatable in a UFT test was limited to 256 columns. This test shows how to open Excel files with up to 16,384 columns. Note that starting with v15, 16,364 columns are supported. However, this script shows how a tester can take detailed control of readying/wriging to Excel spreadsheets, which goes well beyond what is available using the UFTOne GUI interface into parameters.  |

## VuGen scripts
| Script Name  | Note|
| ---------------- | ---------------------------------- |
|[TruClient Native Mobile    ](https://github.com/admpresales/AOS_TruClient_buy_headphones_with_transactions) | This is a simple TruClient mobile script for iOS. Works against the AOS app|
|[vugen-correlation-examples](https://github.com/admpresales/vugen-correlation-examples.git) |This repository contains two VuGen scripts, which contain correlations of increasing complexity. It also contains a PowerPoint presentation which explains correlation in general, and what is in these scripts in particular.|

## Utility scripts
| Script Name  | Note|
| ---------------- | ---------------------------------- |
|[jenkins-jobs](https://github.houston.softwaregrp.net/AMSPreSales-Demos/jenkins-jobs)|This is a set of scripts to extract or deploy Jenkins views and jobs.  It also contains the jobs and views from the released version of the devops docker image|
|[Docker Server Scripts ](https://github.com/panama69/DockerScripts.git)|Scripts used to start various containers for the demos|
|[uft-gui-alm-load-qcp-files](https://github.com/admpresales/uft-gui-alm-load-qcp-files.git)|This utility script was written to enable TE to easily load multiple .qcp files into ALM from the administration web page.

## Branching and Merging strategies
[A Successful Git Branching Model](http://nvie.com/posts/a-successful-git-branching-model/)

[Tags & Releases](https://softwareengineering.stackexchange.com/questions/255404/how-to-use-github-branches-and-automatic-releases-for-version-management)

[Git Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)

[Git Tip: Tags](http://alblue.bandlem.com/2011/04/git-tip-of-week-tags.html)

## How to add a test script to devops container
If you can connect to https://www.github.com from your devops container, then from a terminal window on NimbusServer with the devops container up, run the following command:

```
docker exec devops bash -c "su -s /bin/bash -c 'git clone --mirror https://github.com/admpresales/aos-web-lft4se.git /gitrepo/aos-web-lft4se' apache"
```

If your container can not connect to the internet, then use these from your command window:

```
git clone --mirror https://github.com/admpresales/aos-web-lft4se.git aos-web-lft4se
```
```
docker cp aos-web-lft4se devops:/gitrepo
```
```
docker exec devops bash -c 'chown -R apache:apache /gitrepo/aos-web-lft4se'
```

**You would of course replace the url and name to the git project you wish to use in the above steps**

## Expectations for those developing new scripts

Note: if you create a new test script that think should be added to the admpresales account, the instructions for transfering are here:<br>
[How to transfer a github repository](https://help.github.com/en/articles/transferring-a-repository#transferring-a-repository-owned-by-your-personal-account)
#### README.md
All projects must have a useful README.md. Help on how to create the README.md using the github markdown language can be found:<br>
* [Mastering Markdown](https://guides.github.com/features/mastering-markdown)
* [Markdown Cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [Basic Writing and Formatting](https://help.github.com/articles/basic-writing-and-formatting-syntax)
* [Markdown Cheat sheet PDF](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

If you are going to be writing a lot of Markdown, or writing something "fancy", you might want to install MarkdownPad, which allows you to develop Markdown on your desktop where you see the "code" and results side by side:<br>
[Markdown editor for your desktop](http://markdownpad.com/news/2013/introducing-markdownpad-2)

To make it work on Windows 10 however, you will also need to install awesomium sdk:<br>
[awesomium sdk](http://markdownpad.com/download/awesomium_v1.6.6_sdk_win.exe)

##### Required sections/outline
| Field Name      | Required(Y/N|Other Comments |
| ---------------- | --------------- | ------------------- |
|Script Name      | Y| Should be same as name of repository, except can use Camel-Case |
|Description | Y | Should be same as github repository description string |
|Table of Contents| N | This is a TOC for the README, in case the README is long |
|Usage| Y | How to use including prerequisites and dependencies |
|Send Feedback | Y |  Email(s) |


#### Best practices
##### General
Scripts should be named: <technology-type-target-short_description>

Examples:

	uft-gui-aos-create_new_account
	vugen-truclient-aos_sanity

Note: For UFT Developer scripts, the format is:

	<technology-IDE-type-target-short_description>

This is important especially for scripts developed with Visual Studio.

If the technology supports it, there should be at least one checkpoint.

If the technology supports it, there should a parameterized value(s).

##### UFT Developer
Test scripts should be verified within both NimbusClient and NimbusServer, on all installed browsers

Only maven projects should be used.

UFT Developer version should be set to use the latest version of UFT Developer by modifying the default pom.xml file. Specifically, in properties create a uftdev.version tag, with a value of RELEASE.


    <properties>
        <uftdev.version>RELEASE</uftdev.version>
    </properties>

Then in each uftdev <dependency>, replace the hard coded version with ${uftdev.version}, as shown here:

    <dependency>
            <groupId>com.hp.lft</groupId>
            <artifactId>sdk</artifactId>
            <version>${uftdev.version}</version>
    </dependency>

##### UFT
Web scripts should always be recorded with Internet Explorer so that the active screen is present.

Test script replay should be against the 3 browsers installed on NimbusClient, i.e, IE, Chrome, Firefox.


##### VuGen

RonK or Michal?
