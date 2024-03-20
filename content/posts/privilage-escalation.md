+++
author = "Dennis Sarovski"
title = "Privilage Escalation"
date = "2023-03-14"
description = ""
# tags = [
#     "markdown",
#     "css",
#     "html",
# ]
# categories = [
#     "themes",
#     "syntax",
# ]
+++

## Information Gathering

What's the OS? What version? What Architecture?

    * cat /etc/*-release
    * uname -i, uname -a
    * lsb_release -a (Debian based OS's)

Who are we? Where are we?

    * id
    * pwd

Who uses the box? What users? (And which ones have a valid shell)

    * cat /etc/passwd
    * grep -vE "nologin|false" /etc/passwd

What's currently running on the box? What active network services are there? 

    * ps aux
    * netstat -antup

What's installed? What kernal is being used?

    * dpkg -l (Debian based OS's)
    * rpm -qa (CentOS / openSUSE)
    * uname -a

Then using this information, we can help answer the following:

    * What user files do we have access to?
    * What configurations do we have access to?
    * Any incorrect file permissions?
    * What programs are custom? Any SUID? SGID?
    * What's scheduled to run?
    * Any hardcoded credentials? Where are credentials kept?
    * ...and many many other questions

Check this site out for more.

https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/