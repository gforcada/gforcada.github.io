Title: zc.buildout tricks
Date: 2015-05-04 00:00
Author: admin
Category: General
Tags: plone, tips, zc.buildout
Slug: zc-buildout-tricks
Status: published

Maybe everyone is already aware of them, but just in case...

[zc.buildout](https://pypi.python.org/pypi/zc.buildout) is *THE* building block that assembles Plone together.

It's been around for quite a while (+10 years) and it has plenty of features.

Two of them which I'm enjoying a lot lately are:

    ./bin/buildout install code-analysis

**install** allows you to override which parts are going to be installed and thus it allows, like in the example above, reduce the amount of packages to fetch and things to build. Which for something like jenkins.plone.org can make quite a lot of sense to use it more and more.

    ./bin/buildout annotate

**annotate** outputs the complete configuration that buildout will use as if it was everything in a single file. This is great for debugging "*why my configuration is overriden or not being used at all*" kind of errors.
