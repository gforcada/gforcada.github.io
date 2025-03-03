Title: Faster tests and python 3
Date: 2016-11-28 21:40
Author: admin
Category: General
Tags: jenkins, plone, python3
Slug: faster-tests-and-python-3
Status: published

# 2x faster

Thanks to the Plone Foundation that is sponsoring a new dedicated server for our [jenkins nodes](http://jenkins.plone.org) (the machines that run our test suite on every change),  
the Plone community is starting to enjoy faster builds (twice as fast!).

If your pull request or jenkins job runs on *Node 5* or *Node 6* you will notice it :-)

Please report any misbehavior on [jenkins.plone.org github project](https://github.com/plone/jenkins.plone.org/issues) if you happen to notice something not working as expected.

***Happy testing!***

# Python 3

As the Zope community is getting closer and closer to make a Zope release Python 3 compatible, us, the Plone community have to step up and do the same.  
For that, we are working on, guess what, a new Jenkins job that will only run the test suite of all packages that are known to work on Python 3 already.

The initial list isn't that big, [roughly 10 packages so far](https://github.com/plone/buildout.coredev/pull/282/files), but as more and more Zope packages are updated, the more Plone packages that can be made compatible as well.

The upcoming Alpine Sprint will be dedicated towards this: getting a Plone version compatible with the current Zope versions, which will eventually lead to this Zope on python 3 target (aimed to be released by the end of next year).

***Happy hacking!***
