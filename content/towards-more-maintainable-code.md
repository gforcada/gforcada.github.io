Title: Towards more maintainable code
Date: 2016-01-30 02:53
Author: admin
Category: General
Tags: code analysis, flake8, jenkins, plone, plone.recipe.codeanalysis, sprint
Slug: towards-more-maintainable-code
Status: published

On [my talk at the Plone Conference 2015](https://www.youtube.com/watch?v=BYtqAKH6ZPQ) ([slides](http://www.slideshare.net/gilforcada/beyond-qa), [talk notes](http://maurits.vanrees.org/weblog/archive/2015/10/gil-forcada-codinachs-beyond-qa) from Maurits) one of my points was that **a written style guide is worth nothing if you can not check/enforce it**.

Who *cares* what a style guide says regarding indentation, dependencies, string quoting, docstrings, handling i18n, etc etc if then one can freely commit changes that go against the said style guide?

Fortunately in Python we already have [pep8](http://pypi.python.org/pypi/pep8) (the tool) and [flake8](http://pypi.python.org/pypi/flake8) (with its great [plugin ecosystem](https://pypi.python.org/pypi?%3Aaction=search&term=flake8&submit=search)). To top it off,  on Plone we already have [plone.recipie.codeanalysis](https://pypi.python.org/pypi/plone.recipe.codeanalysis). **We have the tools.**

*Talk is cheap*

I've been putting as much effort and free time as I could to make that happen.

plone.recipe.codeanalysis has been improved ((and by no means only by me)), flake8 plugins have been written, and finally during this last [Alpine City Strategic Sprint 2016](http://gil.badall.net/2016/01/30/alpine-city-strategic-sprint-2016-personal-report/) I could implement the missing piece: **report back to the users** ([see an example](https://github.com/plone/plone.app.contentlisting/commit/6667d607a38e05923218b1ff5953e10efca13326))!

The script is fairly simple:

    #!/usr/bin/env bash
    wget https://raw.githubusercontent.com/plone/buildout.coredev/5.0/bootstrap.py -O bootstrap.py
    wget https://raw.githubusercontent.com/plone/buildout.coredev/5.0/experimental/qa.cfg -O qa.cfg
    wget https://raw.githubusercontent.com/plone/plone.recipe.codeanalysis/master/.isort.cfg -O .isort.cfg
    python bootstrap.py -c qa.cfg
    bin/buildout -c qa.cfg
    bin/code-analysis

Run the above on any Plone distribution and see the output collected on parts/code-analysis/flake8.log

Currently only [a few packages are checked](http://jenkins.plone.org/view/Pkgs/), but cleanup tasks can start on any Plone package as of now. Be sure to [ask for a job](https://github.com/plone/jenkins.plone.org/issues/new) that will check that the package remains clean as soon as your cleanup changes are merged!

**Keep on!**
