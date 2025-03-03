Title: python 3 support one (of the many) step closer
Date: 2016-06-01 23:35
Author: admin
Category: General
Tags: ansible, jenkins, plone, python, python3, ubuntu, vagrant
Slug: python-3-support-one-of-the-many-step-closer
Status: published

During the Barcelona sprint (report from [Paul](http://polyrambling.tumblr.com/post/144601494410/barcelona-2016-sprint-update) and [Ramon](http://bloc.jardigrec.cat/2016/05/what-are-we-doing-in-ploneng-barcelona.html)) there was quite some work to bring dexterity related packages to work both in python 2.7 and python 3.5.

That work is mostly still pending to be merged, because we had a blocker: our current CI infrastructure (namely jenkins master and its nodes) run on a version of Ubuntu ((14.04 for the curious)) that does not provide python 3.5 by default.

So it would be a bit irresponsible to merge those changes without a way to ensure that the effort that was put during that sprint is not long forgotten and had to be done again from scratch some months later.

As reports about the newer Ubuntu version regarding python and plone [are not that encouraging](https://community.plone.org/t/2059), and also due to [other reasons](https://github.com/plone/jenkins.plone.org/issues/170), I decided to take the longest but long-term best approach: enters **[gforcada.compile-python](https://galaxy.ansible.com/gforcada/compile-python/)**!

# An ansible role

So I decided to create an ansible role, given that our [jenkins](https://github.com/plone/jenkins.plone.org/blob/master/jenkins_server.yml) [CI](https://github.com/plone/jenkins.plone.org/blob/master/jenkins_node.yml) setup is already using some, and Plone community is also [favoring it](https://github.com/plone/ansible-playbook), to install all the system dependencies to compile Python 2.6, 2.7 and 3.5.

As extras I added:

- install virtualenv on python 2.6 and 2.7 (on python 3.5 is already available)
- install system dependencies for Pillow and lxml

See its [README](https://galaxy.ansible.com/gforcada/compile-python/) for all the details and more.

With that and vagrant I was able to test that a buildout.coredev (branch 5.1) runs all its tests without a problem :-)

I was tempted to add pypy as well, but I was too lazy/busy for that, if anyone feels like it, [pull requests](https://github.com/gforcada/ansible-compile-python/pulls) are always welcome!

I hope you find it useful and *happy hacking!*
