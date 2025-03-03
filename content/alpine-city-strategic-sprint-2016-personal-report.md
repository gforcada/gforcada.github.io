Title: Alpine City Strategic Sprint 2016 - personal report
Date: 2016-01-30 02:08
Author: admin
Category: General
Tags: collective.indexing, innsbruck, jenkins, plone, sprint
Slug: alpine-city-strategic-sprint-2016-personal-report
Status: published

This past five days I had the pleasure the be part on the last Plone sprint: [Alpine City Strategic Sprint 2016,](http://www.coactivate.org/projects/alpinecitysprint-2016/project-home) **what a blast!**

In the following days, *the amazing never running out of steam*, [Jens](https://github.com/jensens) will report back to [the community](http://community.plone.org/). A partial/preview report [already exists](http://www.coactivate.org/projects/alpinecitysprint-2016/topics-being-worked-on) for the impatient ones (disclaimer: I made it, so there's probably quite a few things missing).

Below I will make a summary of what I achieved thanks to being part of the sprint.

# Work done

## Jenkins/CI

- bring back **[node4 on Jenkins](http://jenkins.plone.org/computer/Node4/)**: meaning that we can run more jobs at the same time, really handy for a sprint or at release time/high activity!
- quickly update (totally untested, so dragons ahead) **ZODB, Zope, ZTK and CMF jenkins jobs**, now they are bundled  together [in a tab](http://jenkins.plone.org/view/Zope/). Pointers on how to make them reliable/improve them highly appreciated, [submit tickets](https://github.com/plone/jenkins.plone.org/issues/new) for it so we can keep track of them
- **create jenkins jobs for PLIPs** [being](http://jenkins.plone.org/view/PLIPs/job/plip-zope4/) [worked](http://jenkins.plone.org/view/PLIPs/job/plip-1334-PlonePAS/) [on](http://jenkins.plone.org/view/PLIPs/job/plip-collective-indexing/) during the sprint. In retrospect they took me less than 5 minutes of work ((thanks to jenkins-job-builder)) and they proved to be extremely helpful. **Pro tip:** whenever working on a new PLIP [ask](https://github.com/plone/jenkins.plone.org/issues/new) for a jenkins job!
- create more [jenkins jobs](https://github.com/plone/jenkins.plone.org/commit/13c1c1fd00b8966379b357079db5f231f97db321) for checking, and reporting back, **code analysis on distributions** (more about it on a follow-up post)

## collective.indexing

Fortunately all the above took less than one or two hours, my main task during the sprint was, together with [Maik](http://github.com/mrtango), bring [collective.indexing in Plone core](https://github.com/plone/Products.CMFPlone/issues/1343) without having to add yet another package ((which our release manager will probably welcome for a change)). Please read the PLIP description, linked above, to know the scope of it.

As of now we are down to [**one single test failure!**](http://jenkins.plone.org/view/PLIPs/job/plip-collective-indexing/20/testReport/) We are highly appreciated on creative ways to solve that last one...

# Not only work

A sprint is way more than just sitting in front of a laptop and coding!

Lots of interesting discussions where held, **we had lots of fun**, we did some sightseeing and enjoyed being together.

And after that I can only say that **Plone's future is brighter than ever has been!**

As a personal pet peeve, we finally [agreed](https://github.com/plone/documentation/pull/509) (?) on how to sort imports! :-)

Last words go to Jens and Christine for taking so much care on preparing everything and being so open and helpful at any time, **thanks!**
