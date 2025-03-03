Title: Robots are taking over
Date: 2016-05-11 23:57
Author: admin
Category: General
Tags: continuous integration, github, jenkins, mr.roboto, plone, pull requests
Slug: robots-are-taking-over
Status: published

Since some time ago [Jenkins](http://jenkins.plone.org), our continuous integration system, already reports back to pull requests the job build status, just like other popular CI systems, there's some documentation on how to trigger [jenkins builds on your pull requests](http://jenkinsploneorg.readthedocs.io/en/latest/run-pull-request-jobs.html).

On selected packages Jenkins is also reporting to GitHub if there are any code analysis errors, see [the list of packages](http://jenkins.plone.org/view/Pkgs/) and [how to run code analysis on your own](http://jenkinsploneorg.readthedocs.io/en/latest/run-qa-on-package.html).

[mr.roboto](https://github.com/plone/mr.roboto) is a [pyramid](http://www.pylonsproject.org/) app that works as a webservice providing integration between our plone/collective GitHub organization and Jenkins.

Some of you might have noticed that **since last week** is adding status updates on pull requests to check if the authors of the pull request have signed the **Plone Contributors Agreement**.

Since **today** it is also checking if pull requests are modifying the **changelog entry** file (namely CHANGES.rst), this way, no change will go unnoticed.

**Next step** is to warn about which **pull requests jobs** need to be run for a given pull request. With the current three major releases (4.3, 5.0 and 5.1) being tested is quite a challenge to know which major versions a pull request should be tested against.

As usual, please report any problem on [jenkins.plone.org issue tracker](https://github.com/plone/jenkins.plone.org/issues/new).

Happy hacking!
