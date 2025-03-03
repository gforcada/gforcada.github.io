Title: Testing pull requests and multi-repository changes
Date: 2015-04-17 22:40
Author: admin
Category: General
Tags: continuous integration, github, jenkins, jenkins-job-builder, plone, pull requests
Slug: testing-pull-requests-and-multi-repository-changes
Status: published

At [Plone](http://www.plone.org "Plone the Open Source Content Management System") we use [Continuous Integration](http://en.wikipedia.org/wiki/Continuous_integration "Continuous integration article at the Wikipedia") (with [Jenkins](http://jenkins-ci.org/)) to keep us aware of any change made on any of our +200 of packages that break the tests.

Thus making it *feasible* to spot where the problem was introduced, find the changes that were made and report back to the developer that made the changes to warn him/her about it.

A more elaborate step by step description is on our [CI rules](http://buildoutcoredev.readthedocs.org/en/latest/continous-integration.html "Plone CI rules"), be sure to read them!

At the same time though, we use GitHub pull requests to make code reviews easy and have a way to provide feedback and context to let everyone give their opinion/comment on changes that can be non-trivial.

Sadly, pull requests and multi-repository changes can not be tested directly with Jenkins, yes, there is a [plugin](https://wiki.jenkins-ci.org/display/JENKINS/GitHub+pull+request+builder+plugin "Jenkins plugin that let's you run test on pull requests") for that, but our CI setup is a *bit* (note the emphasis) more complex than that...

Fortunately we came up with **two solutions** (it's Plone at the end, [we can not have only *one* solution](http://www.slideshare.net/gilforcada/plone-conf2014codeanalysis/11) :D)

# Single pull requests

If you have a pull request on a core package that you want to test follow these steps:

1.  Get the **pull request URL**
2.  Go to <http://jenkins.plone.org> and login with your GitHub user
3.  Go to **pull-request job**: <http://jenkins.plone.org/job/pull-request> (you can see it always at the front page of jenkins.plone.org)
4.  Click on the **Build with Parameters** link on the left column
5.  Paste the pull request URL from *\#1 step*
6.  Click on **Build**

Once it runs you will get an email with the result of the build. If everything is green you can add a comment on the pull request to let everyone know that tests pass.

**Note:** it's your responsibility to run that job with your pull request and that changes made on other packages after tests started running can still make your pull request fail later on, so even if the pull-request job is green, be sure to keep an eye on the main jenkins jobs as soon as you merge your pull request.

Example: Remove Products.CMFDefault from Products.CMFPlone (by @[tomgross](https://github.com/tomgross))

Pull request: <https://github.com/plone/Products.CMFPlone/pull/438>

Jenkins job: <http://jenkins.plone.org/job/pull-request/80>

# Multi-repository changes

When the changes, like massive renamings for example, are spread over more than one repository the approach taken before doesn't work, as the pull-request Jenkins job is only able to change one single repository.

But we, the CI/testing team, have another ace on our sleeves: create a buildout configuration in the **plips** folder on **buildout.coredev** (branch 5.0) that lists all your repositories and which branch should be used, [see](https://github.com/plone/buildout.coredev/blob/5.0/plips/plip-ptc.cfg) [some](https://github.com/plone/buildout.coredev/blob/5.0/plips/plip-nocmfdefault.cfg) [examples](https://github.com/plone/buildout.coredev/blob/5.0/plips/plip-pat-modal.cfg).

Once you have that **cfg** file, you can politely ask the CI team to create a Jenkins job for you. They will make ~~a lot of clever things to make that work on jenkins~~ ([3 lines change](https://github.com/plone/jenkins.plone.org/commit/f4038a086e08db89593970ba62e4a7b8f3b79cdd) plus [following some instructions](http://jenkinsploneorg.readthedocs.org/en/latest/setup.html)) and sooner or later a new Jenkins job will show up on the [PLIPs tab on jenkins.plone.org](http://jenkins.plone.org/view/PLIPs/).

*Rinse and repeat!*

# Extra bonus and caveats

All Jenkins jobs, be it the pull-request, PLIPs and of course the core jobs, are configured to send an email to the one that triggered the job, so don't worry about how long do they take to run, once they are finished you will get notified.

The caveat is that the above is only valid for changes targeting Plone 5. We didn't put the extra effort to make it sure it also works for pull requests (either single or multi-repository) aimed at Plone 4.3. It's quite trivial to add it for multi-repositories, a bit more work to make it run on single pull requests, still feasible to do if there's enough people asking for it.

Hopefully the amount of pull requests for Plone 4.3 will decrease more and more as Plone 5 is getting closer and closer one pull request at a time :)

Now there's **no excuse** on pushing changes to master without having tested them before on jenkins.plone.org!

Proposals on improvements and suggestions are always welcome on the [issue tracker for jenkins.plone.org](https://github.com/plone/jenkins.plone.org/issues) GitHub repository. Help on handling all those issues are, *of course*, also welcomed!

*Happy testing!*
