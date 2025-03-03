Title: Updates from the plone testing and continuous integration team
Date: 2017-04-30 15:30
Author: admin
Category: General
Slug: updates-from-the-plone-testing-and-continuous-integration-team
Status: published

If there's one thing that sprints are for that is to *bootstrap your motivation and engagement with the project*.

So after a really discussion fruitful [PLOG sprint](https://plone.org/events/plone-open-garden-in-sorrento-italy-2017) in beautiful Sorrento (Italy) with amazing food and weather.

With all that energy, and being alone at home without wife nor kid, truth be told, I couldn't stop myself and did some more than needed cleanup and enhancements on [jenkins.plone.org](http://jenkins.plone.org).

# Clean up

Is always a good idea to tidy up your desk before starting to work, *right?*

So one of the first tasks I set up to do was to update the vagrant configuration we have for testing jenkins locally, went over the documentation to double check that everything was correct and while at it iron out everything that on the docs did not make sense to something that hopefully makes a bit more sense.

On that front, the ansible roles used to build both jenkins master and its nodes have been greatly simplified and now, *finally*, others than myself would be able to update jenkins nodes and master without much hassle. If anyone wants to join the team and work on jenkins, please reach out and let's work together!

# Less is more

If you look at Jenkins now you will see that there are *only* 3 nodes, while some weeks ago there where 6.

Workers 1 to 4 where the old and slow ones running on Rackspace still on Ubuntu 14.04 and starting to crash randomly ((node 1 was down already for quite a while and 2 and 4 started failing this weekend as well)).

So I created another node in the new server that the Plone Foundation generously is paying and removed all the old ones.

So while there are less nodes available, [they are much faster](http://gil.badall.net/2016/11/28/faster-tests-and-python-3/) than  before, so hopefully that makes it even.

Stay tuned though, as there is another node coming over if some technical details can be sorted out first.

# Is that compatible?

For quite a while I had this idea floating on my head: it would be cool that add-on developers could check if their add-ons work, not only for the current released Plone version ((that's already doable and easy to set up)), but actually with the current development version.

With that in mind these three new Jenkins jobs were born:

- [Test an add-on against Plone 4.3](http://jenkins.plone.org/job/test-addon-4.3/)
- [Test an add-on against Plone 5.0](http://jenkins.plone.org/job/test-addon-5.0/)
- [Test an add-on against Plone 5.1](http://jenkins.plone.org/job/test-addon-5.1/)

I just did some basic testing on them, so please, use them and report feedback.

*Happy hacking!*
