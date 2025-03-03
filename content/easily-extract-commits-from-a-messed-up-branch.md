Title: Easily extract commits from a messed up branch
Date: 2016-11-02 15:40
Author: admin
Category: General
Tags: git, plone, tips
Slug: easily-extract-commits-from-a-messed-up-branch
Status: published

Once in a while you encounter branches that are have been *over*-used, i.e. multiple persons added commits there for unrelated issues.

**How to get around/solve that?** I'm glad you ask :-)

Today I was facing something similar at work, where the messed up branch in question had some commits already merged into master but there were some important other parts to be extracted from it.

So I used three tools:

- `git log --graph --decorate --pretty=oneline --abbrev-commit --all` (with an alias `git fulllog`)
- a git graphical visualizer ([gitg](https://wiki.gnome.org/Apps/Gitg) for instance)
- a simple plain text editor ([gedit](https://wiki.gnome.org/Apps/Gedit) for instance)

**Workflow**

Fire up `git fulllog` in a terminal and copy & paste as much information as you need into the text editor.

Fire up the git graphical visualizer and check each relevant commit what's doing.

Once you know what it is about annotate each commit so you know which commits relate together, i.e. from

`ae0ee04 My commit message`

to

`ae0ee04 11111 My commit message`

This way once everything is annotated is really simple to just grab all the `11111` commits and `git cherry-pick` them in a new branch :-)

Pro tip: as you are editing a plain text file you can keep removing lines and adjusting the indentation, suddenly you realize how things keep fitting together!

**Done!**
