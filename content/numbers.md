Title: Numbers
Date: 2016-03-02 02:06
Author: admin
Category: General
Tags: code analysis, github, jenkins, plone, plone.recipe.codeanalysis, pull requests
Slug: numbers
Status: published

# 0 to 1k

Yesterday marked the day that Jenkins Job "[Pull Request 5.0](http://jenkins.plone.org/job/pull-request-5.0/)" hit the 1000 job (right now running the 1016!).

It's been a long journey to get it to its current status ((be able to run 4.3 or 5.0 pull requests, allow multiple pull requests per job, report before and after to github just like Travis, allow external forks to be tested...)) but IMHO since the introduction of it our three main Jenkins Jobs for both 4.3 and 5.0 have been far more stable.

**Thanks to everyone that reported feedback and is using it!**

# 100k to 0?

Jenkins is not only about tests, code analysis and all other kind of jobs are running on <http://jenkins.plone.org>. Two of the latest additions are:

- [per package code analysis jobs](http://jenkins.plone.org/view/Pkgs/) that report back to github: packages can opt-in (([fill an issue](https://github.com/plone/jenkins.plone.org/issues/new)!)) and are checked with flake8 and other tools (([more about it](http://gil.badall.net/2016/01/30/towards-more-maintainable-code/)))
- a **global** [code analysis job](http://jenkins.plone.org/view/QA/job/qa-code-analysis/): exactly the same as the per package jobs mentioned on the previous point, but running code analysis on **ALL** packages

The 100k is the flake8 error count for the global job, will we be able to bring that down to zero? :-)

Side note: Zope2 and CMFCore are the two (by far) with more code analysis errors, some other packages are probably going to be deprecated so there is no need to clean up them.

**Best of both things?**

**Anyone (you!?)** can grab a package [clean it up](http://gil.badall.net/2016/02/05/make-code-analysis-cleanups-brainless/), and run a pull request job to ensure nothing is broken after the clean up and happily merge it.

Happy hacking!
