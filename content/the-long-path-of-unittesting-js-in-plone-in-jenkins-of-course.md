Title: the long path of unittesting JS in Plone (in Jenkins of course)
Date: 2015-05-28 22:30
Author: admin
Category: General
Tags: javascript, jenkins, mockup, plone, testing
Slug: the-long-path-of-unittesting-js-in-plone-in-jenkins-of-course
Status: published

One of the main goals of [Mockup](https://github.com/plone/mockup) (the *new* JavaScript story for [Plone](http://plone.org)) is to unittested.

Before Mockup there was no systematic way to unittest JavaScript, you could only do some really slow integration tests via [Robot Framework](http://robotframework.org/) (with its Plone integration [plone.app.robotframework](https://pypi.python.org/pypi/plone.app.robotframework)).

Now with Mockup he have the other side of the coin as well: we can not only check how the code  integrates within Plone but we can also check its logic with fast unittests.

There's already Travis integration for Mockup and Mockup-core (a building block for Mockup), but as Plone is using Jenkins it makes a lot of sense to run them there as well.

So, *how that's done?* I'm glad you ask, **exactly** like this:

1.  Add [Nodejs](http://nodejs.org) on Jenkins nodes ([plone.jenkins_node](https://github.com/plone/plone.jenkins_node/pull/4))
2.  Configure [Jenkins](https://github.com/plone/plone.jenkins_server/pull/17) so that tests will find where Nodejs is ([plone.jenkins_server](https://github.com/plone/plone.jenkins_server/pull/17))
3.  Configure [Grunt](http://gruntjs.com/) (a JavaScript test runner) for Jenkins ([mockup-core](https://github.com/plone/mockup-core/pull/29))
4.  Add a make target for the new Grunt configuration ([mockup](https://github.com/plone/mockup/pull/504))
5.  Create a Jenkins job that runs it ([jenkins.plone.org](https://github.com/plone/jenkins.plone.org/pull/109))
6.  Profit!

All the code is there, the last three pull requests are pending to be merged.

Once that's done [jenkins.plone.org](http://jenkins.plone.org) will be able to run our JavaScript unittests!!

Happy hacking!

P.D: remember that tomorrow is [WPOD](https://community.plone.org/t/world-plone-office-day-wpod/541)!
