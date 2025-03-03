Title: Improvements on Damned-Lies
Date: 2011-08-20 10:38
Author: admin
Category: General
Tags: damned-lies, GNOME, planet GNOME
Slug: improvements-on-damned-lies
Status: published

After the always good [Desktop Summit 2011 in Berlin](http://www.desktopsummit.org "Desktop Summit 2011 website") and having a well deserved holidays afterwards I've already back at home from Germany.

*And* since I have still some days left I started working on fixing one missing feature on **[Damned-Lies](http://l10n.gnome.org "Translation statistics for GNOME")**:

## Word Counting

As of now we have already working [word countings on D-L](https://bugzilla.gnome.org/show_bug.cgi?id=125593 "Bug tracking word countings for Damned-Lies"), a bug opened on **2003!!** ((On the UI front we are still discussing where to show them, you are more than welcome to add your opinions [to the bug created for that](https://bugzilla.gnome.org/show_bug.cgi?id=656938 "Bug for discussing where to show word count statistics"))).

These means that all translators will now more precisely how much effort does it take to translate a module. This is even more useful on documentation, where **1729** strings from the new [Evolution documentation](http://l10n.gnome.org/module/evolution/ "Evolution translation statistics") sure are quite a few strings, like for example [Anjuta UI](http://l10n.gnome.org/module/anjuta/ "Anjuta translation statistics") (which has **1985** strings), but a quick look of how much words each have reveals a huuuge gap between them: **22645** words for Evolution and **7802** words for Anjuta.

I expect that when we start showing word counts on D-L UI translators will have more data to better organize their efforts towards translating GNOME.

I'm already fixing/improving other areas and hopefully I will blog about them soon :) If you have any particular bug/feature missing on Damned-Lies please leave a comment or [file a bug](https://bugzilla.gnome.org/enter_bug.cgi?product=damned-lies "File a bug for Damned-Lies on GNOME's bugzilla")!
