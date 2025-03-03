Title: Berlin 2016 sprint update
Date: 2016-05-20 11:20
Author: admin
Category: General
Tags: berlín, in-berlin, mr.roboto, plone, sprint, zodb, zope
Slug: berlin-2016-sprint-update
Status: published

This week some Plonistas, unfortunately fewer than expected, meet at [IN-Berlin](http://in-berlin.de/) to work towards a brighter future for Plone.

Some of us resumed our work already started in Innsbruck sprint early this year while some other topics grew out of discussions and trying things out.

I will never get to write as good as [Paul reporting on Barcelona's sprint](http://polyrambling.tumblr.com/post/144601494410/barcelona-2016-sprint-update), but hey, I will do my best:

In no special order:

Just by trying out the newly shiny [plone.org](http://plone.org) website (congrats plone.org team!!), some bugs where discovered [and reported](https://github.com/plone/plonetheme.barceloneta/issues), work done by *Stephan Klinger.*

The PLIP about [assimilating collective.indexing](https://github.com/plone/Products.CMFPlone/issues/1343) to Plone core finally got all its tests green and is about to be ready for review, work done by *Maik Derstappen* and *Gil Forcada*.

Python 3 support was a hot topic during the sprint, so with that in mind *Florian Pilz* and *Michael Howitz* created a new tool, [zodb.py3migrate](https://github.com/gocept/zodb.py3migrate), that allows you to convert existing ZODB databases to python 3! Best of all, its [great documentation](http://pythonhosted.org/zodb.py3migrate/)! Be aware that the migration is done in place!

Our Jens<sup>2</sup> team was not quadratic this time around, but *Jens Vagelpohl* continued trying to *tame* Pluggable Authentication Service (aka PAS).

Did I say that Python 3 was a hot topic? *Thomas Lotze* with googling support from *Gil Forcada* took the problem head on and decided that, as Thomas had not that much time (unfortunately he was around only 3 days), work on cracking hard nuts: **C extensions**. And indeed he did! [AccessControl](https://github.com/zopefoundation/AccessControl/pull/17) and [DocumentTemplate](https://github.com/zopefoundation/DocumentTemplate/pull/1) at least compile on python 3.5 (throwing quite some warnings, but hey, have you ever seen Archetypes being installed?). Best of all is that Python 2.6 and 2.7 already have quite some macros for forward compatibility, so the bits that are compatible were pull requested and they are already merged!

Unfortunately that work, C extensions, came to a halt as we hit with RestrictedPython. After long discussions between *Thomas, Gil* and *Maik* we decided to make a video conference with the Barcelona sprint, *Eric Bréhault*, as well as *Alexander Loechel,* who couldn't join is in Berlin, but that he already had worked on the topic while in Insbruck early this year ([read about his findings](https://github.com/zopefoundation/RestrictedPython/blob/Python3_update/docs/update_notes.rst)). The discussion went really well and Alexander offered himself to continue working on it, *stay tuned*!

*Maik* and *Stephan* meanwhile where not happy with the constellation of form packages that we currently have (z3c.form, plone.autoform, plone.supermodel, plone.z3cform, plone.app.z3cform...) and made [yet another package](https://github.com/staeff/example.form) ((will be soon moved to collective))... just kidding! No, instead they worked on improving the forms related documentation: getting rid of grok ((and hidden grok dependencies lying in plone.directives.form and plone.directives.dexterity)) and making sure that the documentation is consistent ((at the beginning there are some fields, and two pages later, magically, fields are different!)). For that Stephan created the linked above package and Maik was working on moving the remaining useful bits of plone.directives.form to plone.autoform. Stephan started a discussion on the topic on [community.plone.org](https://community.plone.org/t/clean-up-documentation-section-schema-driven-forms/2163).

Lastly, I put my jenkins/mr.roboto hat on and added some more functionality to mr.roboto: warn which pull request jenkins jobs need to ran to know if a pull request can be safely merged and auto update buildout.coredev's checkouts.cfg whenever a pull request gets merged. The logic is fairly trivial, but gathering all the pieces together to drive the control is far from it, and testing is yet a complete other matter (thanks [mock](https://pypi.python.org/pypi/mock)!!).

All in all we had fun, lots of things got done or discussed and, as with every sprint, everyone is looking for the next one!

Happy hacking!

 
