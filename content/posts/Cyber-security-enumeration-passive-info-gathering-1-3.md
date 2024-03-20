+++
author = "Dennis Sarovski"
title = "Cybersecurity Enumeration: Passive Information Gathering 1/3"
date = "2023-02-06"
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

In this article, we will delve into the world of cyber security and discuss various techniques and tools that can aid in capturing the flag in CTFs or enhancing one's overall knowledge in this field. It is important to note that the domain of cyber security is vast and constantly evolving, with new technologies and techniques emerging regularly. Therefore, staying up-to-date with the latest developments and trends is crucial for anyone interested in this field.

Some of the key tools and techniques that one should familiarize themselves with include penetration testing, vulnerability scanning, and ethical hacking. In addition, a deep understanding of programming languages such as Python and C++, as well as the basics of networking and operating systems, can also greatly benefit those looking to enhance their cyber security knowledge.

This article series will focus on the crucial aspect of passive information gathering in the field of cyber security. The information will be presented in a comprehensive manner, divided into three separate articles to cover various tools and techniques. Stay tuned for an in-depth exploration of the tools and methods used in passive information gathering, a crucial component of any cyber security strategy.

# What is Passive Information Gathering?

Passive information gathering is an essential component of any cyber security strategy, as it allows for the collection of information about a target without direct interaction. The process involves the use of various tools, such as shodan.io, that provide valuable insights into the target's assets, vulnerabilities, and potential weaknesses.

This type of information gathering is particularly important for specific types of penetration testing, as it enables you to remain undetected by IDS's, firewalls, and logging systems. By reducing direct communication with the target and relying on third-party information, you maintain a high degree of confidentiality and secrecy.

In this article, we will delve into the world of passive information gathering and introduce three essential tools - Whois, Google Hacking, and Netcraft.

By utilizing these tools, cyber security professionals can gain a deeper understanding of the target's assets, network structure, and potential points of vulnerability, thus enabling them to design effective strategies to protect their clients' sensitive information and assets.

# Tool: Whois

Whois is a widely used TCP protocol for querying databases that store information related to domain records. Regulated by ICANN, Whois provides a wealth of information about domain name registration, ownership, and contact information.

With Whois, it's possible to retrieve critical details about a domain, including its name server and the entity responsible for its registration. By utilizing this tool, cyber security professionals can gain valuable insights into a target's domain ownership, network infrastructure, and other relevant information.

As a crucial tool in passive information gathering, Whois can be an integral part of any successful cyber security operation. Get ahead of the game and master the use of Whois in your information gathering efforts today.

Here's an example of running Whois against the domain 'example.com':

![alt text](/posts/enum-passive-1-3/image.png)

By conducting a Whois query on a target domain, one can gather information such as name servers, domain registration details, and potentially even personally identifiable information. This information can then be used as a starting point for further investigations and to develop more comprehensive cyber security strategies.

It's important to note that not all information retrieved from a Whois query may be useful, as some information may be hidden by the DNS provider. However, even partial information can be beneficial and lead to further discovery. In the field of cyber security and blogging, utilizing Whois is a key aspect of passive information gathering and essential for developing effective and targeted security strategies.

# Google Hacking

Google Hacking, also known as Google Dorking, is a valuable technique in the realm of cyber security. It involves leveraging search engines to uncover sensitive information about a target, including vulnerabilities, misconfigured websites, login credentials, and financial data.

Google Hacking is achieved by utilizing various search operators offered by search engines such as Google. These operators can be used to conduct advanced searches, enabling the discovery of potentially sensitive information. The use of these operators is a critical aspect of Google Hacking and is a crucial tool for those looking to stay ahead in the ever-evolving world of cyber security.

    * site: - limit search to a specific website, e.g. site:example.com

    * filetype: - search for specific file types, e.g. filetype:pdf

    * intitle: - search for keywords in page title, e.g. intitle:"best restaurants"

    * inurl: - search for keywords in URL, e.g. inurl:"best hotels"

    * link: - search for pages that link to a specific URL, e.g. link:example.com

    * related: - search for websites related to a specific URL, e.g. related:example.com

    * cache: - show Google's cached version of a page, e.g. cache:example.com

    * define: - search for definitions, e.g. define:happiness

    * info: - display information about a specific URL, e.g. info:example.com

    * allintitle: - search for pages with all search terms in the title, e.g. allintitle:best restaurants in town

By utilizing these advanced search operators, cyber security professionals and ethical hackers can effectively narrow down their search results and obtain targeted information about their target. For instance, the site operator can be utilized to search for a specific website, such as in the example of searching for 'site:example.com'

![alt text](/posts/enum-passive-1-3/image-1.png)


# Tool: Netcraft

Netcraft is a leading provider of web security and technology solutions, offering a range of internet services and tools. One of their most renowned offerings is the Netcraft Toolbar - a browser extension that provides insightful information about websites, including the technologies used, hosting location, and ownership details.

With their free web portal, users can access a variety of information-gathering functions using a passive technique, without ever directly interacting with their target. Searchdns.netcraft.com is a valuable resource for searching DNS results of any website you wish to know more about. For instance, searching "example.com" will provide you with relevant results.

![alt text](/posts/enum-passive-1-3/image-2.png)

By clicking on the "Site Report" option, you can access more information about the website. This information includes a wide range of details, such as background information, network details, IP delegation, SSL/TLS information, hosting history, and more.

![alt text](/posts/enum-passive-1-3/image-4.png)

![alt text](/posts/enum-passive-1-3/image-5.png)

![alt text](/posts/enum-passive-1-3/image-6.png)


I hope these tools and sites assist you in expanding your knowledge of Passive Information Gathering. Stay tuned, as I will be posting further updates on this subject in the near future, including additional tools and techniques to utilize.