Title: PTotD
Date: 2012-08-24 09:09
Author: admin
Category: General
Tags: planet GNOME, python, traduccions
Slug: ptotd
Status: published

... also known as *Python Tip of the Day*:

What's wrong (translation-wise) on this snippet of python code?

    random = _("Lorem ipsum dolor sit amet, " +
               "consectetur adipisicing elit")

You are not going to see any warning on your code, if you don't have this message translated you will never notice...

But unfortunately, as soon as you have this message translated you will notice that only half of the string is translated, which for Arabic or other RTL ((Right to Left)) languages can be quite funny...

So, you already noticed right?

Turns out that gettext gets confused by the **plus sign**! As you already may remember by now, Python can join multiple strings just by putting them together, no need for a plus sign. Try it yourself on your python console:

    >>> print ("Lorem " " ipsum" " dolor"
    ... " amet")
    Lorem  ipsum dolor amet

So dear Python developers out there, pretty please double check your strings marked for translation, if not a translator will find out, hopefully before a release, and [report it back](https://bugzilla.gnome.org/show_bug.cgi?id=682275 "PiTiVi had that bug :)") :)

## Planet GNOME

Seems that I pestered enough our (that sound good!) [planet editor](http://aruiz.typepad.com/ "Alberto Ruiz's blog") ((Wo was so nice to also create my planet hackergotchi!)) that he finally [added me in](https://bugzilla.gnome.org/show_bug.cgi?id=656963 "Bug requesting me being added to p.g.o"). Hi GNOMEr's around the globe!!

I'm Gil Forcada, [Coordinator of the Catalan Translator Team](http://l10n.gnome.org/languages/ca "GNOME Catalan Translation team page "), member of the [Localization Coordination Team](https://live.gnome.org/TranslationProject/CoordinationTeam "Wiki page with the list of Translation Coordination Team members"), nowadays also [Damned-Lies](http://l10n.gnome.org "Translation statistics website for GNOME") maintainer and usually you see me on GUADEC's behind the info desk :D

I'm all digital ears to digitally hear anything related to l10n/i18n and how to move GTP ((GNOME Translation Project)) forward!

**Edit:** fixed the \\ on the second code snippet (no need for that) and the LTR to RTL! Oh my!
