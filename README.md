# Updating-to-4.0.0-on-MacOS

The details of the codeset and plots are included in the attached Adobe Acrobat reader (.pdf) file in this repository. 
You need to download the same to view the contents. There are referrals to other contents in BLUE colour also to follow.

A Brief Introduction
=====================

Mixed emotions

Wow! Has it been a year? Another major update from The R
Foundation (the recent 4.0.0 release in April). I’m always happy to see the
continuing progress and the combination of new features and bug fixes, but I
also dread the upgrade because it means I have to address the issue of what to
do about the burgeoning number of packages (libraries) I have installed. I wrote
a fairly comprehensive post about it last year. I just took the plunge this year
and almost everything seems to still work. Vindication!

I’m aware that there are full-fledged package managers [https://blog.learningtree.com/manage-packages-in-r-how/]
like packrat and checkpoint and even a package designed to manage the upgrade for
you on windows, but I’m a Mac user and wanted to do things my own way and I
don’t need that level of sophistication.

So I set out to do the following:

    Keep a copy for my own edification and potential future use.
    Do a clean R 4.0.0 install and not copy any library directories manually or
    create symlinks or any other thing at the OS level.
    Take a look at the list I produced in #1 above but mainly to just download
    and install the exact same packages if I can find them.
    Make the process mainly scripted and automatic and available again for
    the future – it worked this year let’s hope it works again next.

Before you upgrade!

Let’s load tidyverse to have access to all it’s various functions and
features and then build a dataframe called allmypackages with the basic
information about the packages I currently have installed in R 3.6.3.
