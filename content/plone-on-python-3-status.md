Title: Plone on python 3 status
Date: 2016-10-23 05:53
Author: admin
Category: General
Tags: plone, plone conference, python, python3
Slug: plone-on-python-3-status
Status: published

2020 is approaching fast, one day at a time, and besides being a nice catchy year, it will be also the year where Python 2.7 [will no longer get any security updates](https://pythonclock.org/).

**What that means for Plone?** We should hurry up and get a python 3 porting of the *whole* stack, yes, including Zope, ZTK, ZODB and all the tooling around (zc.buildout, etc etc).

Fortunately quite some tooling and Zope/ZTK/ZODB is already updated and there's ongoing effort on porting the remaining parts.

The big elephant on the room blocking any porting effort of Plone to python 3 was [RestrictedPython](https://pypi.python.org/pypi/RestrictedPython), a python distribution that, quoting itself: *provides a restricted execution environment for Python*.

**Note the past on the previous sentence.**

Since RestrictedPython is being worked, now it's high  time for the other python distributions from Plone to be also made compatible with Python 3. Stay tuned for the [Plone Conference 2016 sprint](https://2016.ploneconf.org/sprints) report!

[Copy&pasting&adapting](https://github.com/collective/ztk-py3-status) a set of [scripts to track the progress](https://github.com/mgedmin/ztk-py3-status) of the porting for the Zope foundation github organization, [results here](http://zope3.pov.lt/py3/), I made the same but tracking what Plone 5.1 (including our testing environment) looks like on Python 3:

### <http://jenkins.plone.org/py3/>

The code is on [collective](https://github.com/collective/ztk-py3-status), so feel free to update the [package list](https://github.com/collective/ztk-py3-status/blob/master/plone_packages.py).

During the Plone Conference 2016  there is quite some work put on either reducing the amount of dependencies, or updating our stack to use newer (already python 3 compatible) part of the underlying stack.

**The clock is ticking and Plonistas all over the world are working hard on it!**
