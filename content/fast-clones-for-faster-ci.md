Title: Fast clones for faster CI
Date: 2015-05-23 16:44
Author: admin
Category: General
Tags: continuous integration, mr.developer, plone
Slug: fast-clones-for-faster-ci
Status: published

Did you ever got tired waiting a repository (managed by mr.developer) to be cloned?

Wait no more! [mr.developer](https://pypi.python.org/pypi/mr.developer) 1.32 comes with two new options to make your life easier:

- a global `git-clone-depth` option that allows to fetch **only** the amount of history specified on this option (i.e. git-clone-depth = 1 for only one single commit)
- a per-source `depth` option that allows to specify the same as git-clone-depth but only for that specific source

What's the benefit of this? See it for yourself:

    git clone https://github.com/plone/buildout.coredev.git test-full
    du -sh test-full
    36M test-full

    git clone https://github.com/plone/buildout.coredev.git --depth=1 test-shallow
    du -sh test-shallow
    1,5M    test-shallow

That's a **24x** saving.

So think about your CI environments where they are downloading over and over the whole repository information while you only care about the very last changes.

Think about some remote environments (mobile connection while you are on a train?)

~~**Update:** it seems that is completely broken, sorry for that, working on a fix.~~

**Update 2:** mr.developer 1.33 released, thanks @fschulze for the new release!
