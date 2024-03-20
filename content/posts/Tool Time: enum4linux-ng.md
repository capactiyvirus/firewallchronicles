+++
author = "Dennis Sarovski"
title = "Tool Time: enum4linux-ng"
date = "2023-02-23"
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

I've learned about many different tools that can be useful for CTF (Capture the Flag) competitions and other security-related activities. In this article, I'll be focusing on one of these tools: enum4linux and its successor, enum4linux-ng.

Both of these tools are designed to help with the enumeration of Windows and Samba systems, allowing security professionals and penetration testers to extract valuable information from SMB shares. Enum4linux has been a popular tool for many years, but the newer enum4linux-ng offers some improvements and additional features that make it a great option for those looking to perform more advanced enumeration.

In this guide, I'll be providing an overview of both enum4linux and enum4linux-ng, highlighting their features and differences. By the end of this article, you should have a good understanding of what these tools are capable of and how they can be used in your CTF and security-related activities.

# What is enum4linux?

Enum4linux is a valuable tool for security professionals and CTF players who need to extract data from Windows and Samba hosts. This tool is built on top of the samba tools smbclient, rpcclient, net, and nmblookup, and provides a user-friendly interface for enumerating information from SMB shares.

Originally written by Mark Lowe, enum4linux has become a staple tool in the security community due to its ease of use and powerful features. With enum4linux, users can easily extract information such as user and group lists, share names, and other important details.

If you're using Kali Linux, you should already have enum4linux installed. However, if you don't have it installed or are using a different operating system, you can use the package manager to install it. Once installed, you can start using enum4linux to enumerate Windows and Samba hosts and gather important information for your security assessments and CTF challenges.

```
sudo apt install enum4linux
```

Once you have installed enum4linux, you can learn more about the tool by exploring the man pages or running the command enum4linux -h. The man pages provide detailed information on how to use the tool, including the various options and arguments that can be used with enum4linux. Running the command enum4linux -h will display a help message that provides a brief overview of the tool and its capabilities, making it a great starting point if you're new to enum4linux and want to get a better understanding of what it can do. By taking the time to explore the man pages and run enum4linux -h, you can gain a deeper understanding of how to use enum4linux effectively and get the most out of its features. This will help you to be better equipped to perform effective enumeration during your security assessments and CTF challenges.

```
└─$ enum4linux -h                                 
enum4linux v0.9.1 (http://labs.portcullis.co.uk/application/enum4linux/)
Copyright (C) 2011 Mark Lowe (mrl@portcullis-security.com)

Simple wrapper around the tools in the samba package to provide similar 
functionality to enum.exe (formerly from www.bindview.com).  Some additional 
features such as RID cycling have also been added for convenience.

Usage: ./enum4linux.pl [options] ip

Options are (like "enum"):
    -U        get userlist
    -M        get machine list*
    -S        get sharelist
    -P        get password policy information
    -G        get group and member list
    -d        be detailed, applies to -U and -S
    -u user   specify username to use (default "")  
    -p pass   specify password to use (default "")   

The following options from enum.exe aren't implemented: -L, -N, -D, -f

Additional options:
    -a        Do all simple enumeration (-U -S -G -P -r -o -n -i).
              This option is enabled if you don't provide any other options.
    -h        Display this help message and exit
    -r        enumerate users via RID cycling
    -R range  RID ranges to enumerate (default: 500-550,1000-1050, implies -r)
    -K n      Keep searching RIDs until n consective RIDs don't correspond to
              a username.  Impies RID range ends at 999999. Useful 
              against DCs.
    -l        Get some (limited) info via LDAP 389/TCP (for DCs only)
    -s file   brute force guessing for share names
    -k user   User(s) that exists on remote system (default: administrator,guest,krbtgt,domain admins,root,bin,none)
              Used to get sid with "lookupsid known_username"
              Use commas to try several users: "-k admin,user1,user2"
    -o        Get OS information
    -i        Get printer information
    -w wrkg   Specify workgroup manually (usually found automatically)
    -n        Do an nmblookup (similar to nbtstat)
    -v        Verbose.  Shows full commands being run (net, rpcclient, etc.)
    -A        Aggressive. Do write checks on shares etc

RID cycling should extract a list of users from Windows (or Samba) hosts 
which have RestrictAnonymous set to 1 (Windows NT and 2000), or "Network 
access: Allow anonymous SID/Name translation" enabled (XP, 2003).

NB: Samba servers often seem to have RIDs in the range 3000-3050.

Dependancy info: You will need to have the samba package installed as this 
script is basically just a wrapper around rpcclient, net, nmblookup and 
smbclient.  Polenum from http://labs.portcullis.co.uk/application/polenum/ 
is required to get Password Policy info.
```

# What is enum4linux-ng?

Enum4linux-ng is an updated version of the popular enumeration tool enum4linux, designed to be more user-friendly and feature-rich. Developed by cddmp, this new version builds upon the strengths of its predecessor while introducing new capabilities to help security professionals and CTF players uncover valuable information from Windows and Samba hosts.

Some of the notable features of enum4linux-ng include improved speed and reliability, expanded capabilities for enumerating data, better compatibility with modern operating systems, and the ability to target specific users or hosts. These features make it an invaluable tool for reconnaissance and vulnerability assessment, allowing users to identify weaknesses in target systems and improve their overall security posture. Some of its new features are:

    * Yaml and Json export

    * colored console output

    * ldapsearch and polenum and implemented

    * support for legacy SMBv1 connections

    * support for multiple authentication methods

    * auto detection of IPC signing support

    * 'smart' enumeration will automatically disable tests which would otherwise fail

    * timeout support

    * SMB dialect checks

    * IPv6 support (experimental)

# Installation

Installing enum4linux-ng is a straightforward process. Simply visit the official GitHub repository at https://github.com/cddmp/enum4linux-ng and clone the repository to your local machine. Once you've done this, ensure that any dependencies required by the tool are installed on your system.

You can verify that you have all necessary dependencies by running the tool and observing any error messages or warnings that may appear. If you encounter any issues during installation or usage, consult the documentation or seek assistance from the tool's online community.

```
pip install -r requirements.txt 
# Just make sure your python version coensides with the accepable versions on the repo.
```


Once you've ensured that all dependencies are installed, you can proceed with installing enum4linux-ng by running the setup.py file. This should automatically install the tool and set it up for usage.

To confirm that the installation was successful, run the command enum4linux-ng -h to access the tool's help menu. From here, you can explore the different options and features available within the tool and learn more about how to use it effectively.

Remember to consult the documentation or seek assistance from the tool's online community if you encounter any issues during installation or usage.

```
└─$ enum4linux-ng -h                              
ENUM4LINUX - next generation (v1.3.1)

usage: enum4linux-ng [-h] [-A] [-As] [-U] [-G] [-Gm] [-S] [-C] [-P] [-O] [-L] [-I] [-R [BULK_SIZE]] [-N] [-w DOMAIN] [-u USER] [-p PW | -K TICKET_FILE | -H NTHASH]
                     [--local-auth] [-d] [-k USERS] [-r RANGES] [-s SHARES_FILE] [-t TIMEOUT] [-v] [--keep] [-oJ OUT_JSON_FILE | -oY OUT_YAML_FILE | -oA OUT_FILE]
                     host

This tool is a rewrite of Mark Lowe's enum4linux.pl, a tool for enumerating information from Windows and Samba systems. It is mainly a wrapper around the Samba tools nmblookup,
net, rpcclient and smbclient. Other than the original tool it allows to export enumeration results as YAML or JSON file, so that it can be further processed with other tools.
The tool tries to do a 'smart' enumeration. It first checks whether SMB or LDAP is accessible on the target. Depending on the result of this check, it will dynamically skip
checks (e.g. LDAP checks if LDAP is not running). If SMB is accessible, it will always check whether a session can be set up or not. If no session can be set up, the tool will
stop enumeration. The enumeration process can be interupted with CTRL+C. If the options -oJ or -oY are provided, the tool will write out the current enumeration state to the
JSON or YAML file, once it receives SIGINT triggered by CTRL+C. The tool was made for security professionals and CTF players. Illegal use is prohibited.

positional arguments:
  host

options:
  -h, --help         show this help message and exit
  -A                 Do all simple enumeration including nmblookup (-U -G -S -P -O -N -I -L). This option is enabled if you don't provide any other option.
  -As                Do all simple short enumeration without NetBIOS names lookup (-U -G -S -P -O -I -L)
  -U                 Get users via RPC
  -G                 Get groups via RPC
  -Gm                Get groups with group members via RPC
  -S                 Get shares via RPC
  -C                 Get services via RPC
  -P                 Get password policy information via RPC
  -O                 Get OS information via RPC
  -L                 Get additional domain info via LDAP/LDAPS (for DCs only)
  -I                 Get printer information via RPC
  -R [BULK_SIZE]     Enumerate users via RID cycling. Optionally, specifies lookup request size.
  -N                 Do an NetBIOS names lookup (similar to nbtstat) and try to retrieve workgroup from output
  -w DOMAIN          Specify workgroup/domain manually (usually found automatically)
  -u USER            Specify username to use (default "")
  -p PW              Specify password to use (default "")
  -K TICKET_FILE     Try to authenticate with Kerberos, only useful in Active Directory environment
  -H NTHASH          Try to authenticate with hash
  --local-auth       Authenticate locally to target
  -d                 Get detailed information for users and groups, applies to -U, -G and -R
  -k USERS           User(s) that exists on remote system (default: administrator,guest,krbtgt,domain admins,root,bin,none). Used to get sid with "lookupsids"
  -r RANGES          RID ranges to enumerate (default: 500-550,1000-1050)
  -s SHARES_FILE     Brute force guessing for shares
  -t TIMEOUT         Sets connection timeout in seconds (default: 5s)
  -v                 Verbose, show full samba tools commands being run (net, rpcclient, etc.)
  --keep             Don't delete the Samba configuration file created during tool run after enumeration (useful with -v)
  -oJ OUT_JSON_FILE  Writes output to JSON file (extension is added automatically)
  -oY OUT_YAML_FILE  Writes output to YAML file (extension is added automatically)
  -oA OUT_FILE       Writes output to YAML and JSON file (extensions are added automatically)
  ```

# Using the tool

Once you've installed enum4linux-ng and familiarized yourself with its usage, running the tool can be as simple as executing the command enum4linux-ng -A <IP>. The -A option tells enum4linux-ng to perform all available enumeration techniques on the target IP address.

Upon running this command, you can expect to see a detailed output that includes information such as the target's hostname, user accounts, group memberships, and various other details about the Samba server.

It's important to note that the exact output and information retrieved may vary depending on the target system's configuration and available services. However, the information gathered by enum4linux-ng can be valuable for conducting reconnaissance and identifying potential vulnerabilities in the target system.

Here is a sample output:

![alt text](/posts/enum4linux-ng/image.png)
![alt text](/posts/enum4linux-ng/image-1.png)