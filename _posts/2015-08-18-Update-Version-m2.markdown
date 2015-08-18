---
layout: post
title:  "Tutora 0.2"
date:   2015-08-18 23:00:00
description: Taking baby steps towards adding functionality
categories:
- blog
permalink: Update-Version-m2
---

Hello again!

As you can see from the title, I moved Tutora from version 0.1
to 0.2 . In general, I won't be posting on this blog for every
minor release I make. This time though, I feel like I've built
some important features in Tutora that will work as stepping
stones for most of its planned future functionality.

To be more specific, the user table has two new fields -
username and pass. It is important to note that the username
will be used only for organization/university email related
functionality and maybe for routing in restricted pages. The
username will not be used as is for authentication when logging
in Tutora. That brings me to my next update.

A login page has been added and it works as expected. Users
can now login by providing their user ID (numeric one, not
their username) and their password. After logging in, a user
can also logout (unlike the kiosk where a person can only
signin but not signout, for the time being).

Furthermore, I added a database-related utility function. When
passed a text file with new user entries, that contain 3 columns
each (ID, username and name), the function parses the file and
imports the user in the database. This function has descent error
handling implemented within it and it comes with its own tests. When
importing a user in the database, a default password is generated
for the user consisting of its username followed by her ID number.
Users should be able to change their password in the future
after logging in for the first time in the future.

As a final major update, passwords are encrypted in the database
now using bcrypt from the Buddy module. There has also been some
minor code cleanup which includes the removal of the about page
which I really couldn't find a reason to keep it around.

What comes next? My promise of implementing the signout and feedback
workflows. After that, I will quickly implement my TODO entry of
increasing the visit counter of a user whenever he signs in and I
will jump to thoroughly test all routing functionality implemented
so far.

Wish me luck!
