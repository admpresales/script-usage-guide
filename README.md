# Script-Directory
This is planned to be a landing page to help expose several demo assets that the field has found useful as part of a core demo or taylored demo.

**Most** of these scripts are not considered as part of the "core" demo assets which means you will **not** find them delivered as part of the [devops.dockerapp](https://hub.docker.com/r/admpresales/devops.dockerapp/) or the [devops](https://hub.docker.com/r/admpresales/devops/) images.  Scripts that are shown on this page that are part of the core scripts delivered in the Devops image are noted with '(c)'.  For example:
```
leanft-gherkin (c)
```

Instructions on [How to add test to devops container](https://github.com/admpresales/script-directory#how-to-add-test-to-devops-container) can be found below.

## UFT Pro (LeanFT) Scripts
| Script Name      | Note                               |
| ---------------- | ---------------------------------- |
| [leanft-gherkin](https://github.com/admpresales/leanft-gherkin) (c)| IntelliJ - maven project which uses LeanFT and gherkins feature file and cucumber for execution.  This one actually executes a test against AOS|
|[octane-gherkin](https://github.com/admpresales/octane-gherkin) (c)|Very similar to LeanFT_Gherkins with the exception that the Gherkin step definitions are left empty so it runs faster.  The intent here is used when focusing on Octane demos only and LFT is not a focus.|
|[aos-web-lft4se](https://github.com/admpresales/aos-web-lft4se) | Maven project demonstrating using LeanFT for Selenium in a simple project.  This was created using the Selenium OIC.|
|[simple-lft-selenium](https://github.com/admpresales/simple-lft-selenium)|Simple script demonstrating Selenium and LFT used together.  With webdriver launching and LFT attaching to browser and using the Verify and Reporter classes|
|[Mobile_AOS_Test](https://github.com/panama69/Mobile_AOS_Test)|Simple LFT test against AOS on an Android device|
|[LeanFT_AppliTools](https://github.com/panama69/LeanFT_AppliTools)|Very simple LeanFT/AppliTools test using C#.  The code came from AppliTools website but I add information to readme to aid in setting things up|
|[LeanFT_Cross_Browser_Mobile](https://github.com/panama69/LeanFT_Cross_Browser_Mobile)|Simple script showing execution across the desktop Firefox browser and the iPhone Safari browser.| 
|[testng-example](https://github.com/admpresales/testng-example)|Simple TestNG tests using LeanFT Reports to demonstrate how to run TestNG in parallel and pass arguments to a test|

## UFT Scripts
| Script Name      | Note                               |
| ---------------- | ---------------------------------- |
|[UFT-Comprehensive-FlightGUI](https://github.com/rsercely/UFT-Comprehensive-FlightGUI)|UFT script demonstrating several capabilites of UFT (courtesy Ron Sercely) |

## Utility scripts
| Script Name      | Note                               |
| ---------------- | ---------------------------------- |
|[jenkins-jobs](https://github.houston.softwaregrp.net/AMSPreSales-Demos/jenkins-jobs)|This is a set of scripts to extract or deploy Jenkins views and jobs.  It also contains the jobs and views from the released version of the devops docker image|
|[Docker Server Scripts](https://github.com/panama69/DockerScripts.git)|Scripts used to start various containers for the demos|

## Branching and Merging strategies
[A Successful Git Branching Model](http://nvie.com/posts/a-successful-git-branching-model/)

[Tags & Releases](https://softwareengineering.stackexchange.com/questions/255404/how-to-use-github-branches-and-automatic-releases-for-version-management)

[Git Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)

[Git Tip: Tags](http://alblue.bandlem.com/2011/04/git-tip-of-week-tags.html)

## How to add test to devops container
&#x1F340; `If you can connect to www.github.com from your devops container, then from a terminal window on NimbusServer with the devops container up, run the following command:`

```
docker exec devops bash -c "su -s /bin/bash -c 'git clone --mirror https://github.com/admpresales/aos-web-lft4se.git /gitrepo/aos-web-lft4se' apache"
```

`If your container can not connect to the internet, then use these from your terminal window`
```
git clone --mirror https://github.com/admpresales/aos-web-lft4se.git aos-web-lft4se
docker cp aos-web-lft4se devops:/gitrepo
docker exec devops bash -c 'chown -R apache:apache /gitrepo/aos-web-lft4se'
```
**You would of course replace the url and name to the git project you wish to use in the above steps**
