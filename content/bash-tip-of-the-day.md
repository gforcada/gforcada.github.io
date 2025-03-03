Title: bash tip of the day
Date: 2012-09-26 15:20
Author: admin
Category: General
Tags: bash, planet GNOME
Slug: bash-tip-of-the-day
Status: published

After spending an hour or so staring at a regular expression in bash, I gave up and started looking at the interwebs... So what's wrong on this?

    random="aabbcc"
    if [[  $random =~ "^a{1,2}b{1,2}c{1,2}$"  ]]; then
        echo "matching"
    else
        echo "not matching"
    fi

It's supposed to compare \$random with a regular expression (that's what's supposed to do the =~ operator). But no matter how hard I tried, it was always "not matching"

Fortunately this days we have stackoverflow [with the answers](http://stackoverflow.com/questions/304864).

 

 

 

 

*(some spacing so that you can think on it....)*

 

 

 

 

 

Short answer: **no quotes around a regular expression!**

I start getting a pattern here (punt intended), the clueless I'm usually while trying to find the solution, the easiest it is :)
