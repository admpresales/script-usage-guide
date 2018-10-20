# Script-Directory
This is planned to be a landing page to help expose several demo assets that the field has found useful as part of a core demo or taylored demo.

**Most** of these scripts are not considered as part of the "core" demo assets which means you will **not** find them delivered as part of the [devops.dockerapp](https://hub.docker.com/r/admpresales/devops.dockerapp/) or the [devops](https://hub.docker.com/r/admpresales/devops/) images.  Scripts that are shown on this page that are part of the core scripts delivered in the Devops image are noted with '(c)'.  For example:
```
leanft-gherkin (c)
```

Instructions on [How to add test to devops container](#how-to-add-test-to-devops-container) can be found below.  Please make sure all projects have a useful README.md on how one should use the script.  Help on how to create the README.md using the github markdown language can be found:
* [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
* [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [Basic Writing and Formatting](https://help.github.com/articles/basic-writing-and-formatting-syntax/)
* [Markdown Cheatsheet PDF](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)

## LeanFT Scripts
| Script Name      | Note                               |
| ---------------- | ---------------------------------- |
| [leanft-gherkin](https://github.com/admpresales/leanft-gherkin) (c)| IntelliJ - maven project which uses LeanFT and gherkins feature file and cucumber for execution.  This one actually executes a test against AOS|
|[octane-gherkin](https://github.com/admpresales/octane-gherkin) (c)|Very similar to LeanFT_Gherkins with the exception that the Gherkin step definitions are left empty so it runs faster.  The intent here is used when focusing on Octane demos only and LFT is not a focus.|
|[aos-web-lft4se](https://github.com/admpresales/aos-web-lft4se) | Maven project demonstrating using LeanFT for Selenium in a simple project.  This was created using the Selenium OIC.|
|[simple-lft-selenium](https://github.com/admpresales/simple-lft-selenium)|Simple script demonstrating Selenium and LFT used together.  With webdriver launching and LFT attaching to browser and using the Verify and Reporter classes|
|[oscillating](https://github.com/admpresales/oscillating)|This script was used as part of a training session to demonstrate how areas of the Octane Pipeline Analysis screen gets populated based on how scripts run, pass, fail, etc.|
|[Mobile_AOS_Test](https://github.com/panama69/Mobile_AOS_Test)|Simple LFT test against AOS on an Android device|
|[LeanFT_AppliTools](https://github.com/panama69/LeanFT_AppliTools)|Very simple LeanFT/AppliTools test using C#.  The code came from AppliTools website but I add information to readme to aid in setting things up|
|[LeanFT_Cross_Browser_Mobile](https://github.com/panama69/LeanFT_Cross_Browser_Mobile)|Simple script showing execution across the desktop Firefox browser and the iPhone Safari browser.| 
|[testng-example](https://github.com/admpresales/testng-example)|Simple TestNG tests using LeanFT Reports to demonstrate how to run TestNG in parallel and pass arguments to a test|

## UFT Scripts
| Script Name      | Note                               |
| ---------------- | ---------------------------------- |
|[flight-api-with-gui-verification](https://github.com/admpresales/flight_api_with_gui_verification)|Demonstrates using API test interacting (calling) GUI test.  This script is great for showing customer the value of using API testing with their regression suites. Much of regression testing is setting up specific data secnarios to users can perform the actual test they need. Using API for the setup can drastically reduce the oveall execution time.|
|[comprehensive-uft-test-flightgui](https://github.com/admpresales/comprehensive-uft-test-flightgui)|UFT script demonstrating several capabilites of UFT (courtesy Ron Sercely) |

## VUGen scripts
| Script Name      | Note                               |
| ---------------- | ---------------------------------- |
|[TruClient Native Mobile](https://github.com/admpresales/AOS_TruClient_buy_headphones_with_transactions)|This is a simple TruClient mobile script for iOS. Works against the AOS app|

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

## Postman Client
[Postman Echo](https://docs.postman-echo.com/)

[Postman Cheatsheet](https://media.readthedocs.org/pdf/postman-quick-reference-guide/latest/postman-quick-reference-guide.pdf)

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
