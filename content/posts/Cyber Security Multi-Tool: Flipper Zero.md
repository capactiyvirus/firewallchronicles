+++
author = "Dennis Sarovski"
title = "Cyber Security Multi-Tool: Flipper Zero"
date = "2023-01-29"
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
#series = ["Themes Guide"]
#aliases = ["migrate-from-jekyl"]
+++

Today, I'd like to share my thoughts on a cutting-edge tool that has recently gained immense popularity in the market and has been making waves on TikTok. Despite being a bit late to the party, I still think this tool is worth mentioning due to its cool features and ability to educate those interested in cybersecurity and the various physical tools available.

The tool I am referring to is a compact, multi-functional device that provides a plethora of features and capabilities to aid in penetration testing and security auditing. With built-in support for wireless network scanning and cracking, password cracking, data analysis, and more, this tool provides an all-in-one solution for those looking to explore the world of cybersecurity.

# What is the Flipper Zero?

The Flipper Zero is a cutting-edge, multi-functional device with a unique and engaging design. This portable device was specifically created to interact with access control systems, providing users with the ability to read, copy, and emulate radio-frequency (RFID) tags, radio remotes, iButton, and digital access keys, all through a GPIO interface.

First announced in August 2020, the Flipper Zero received widespread recognition and support through its successful Kickstarter crowdfunding campaign, raising a staggering $4.8 million. The devices were delivered to backers 18 months after the successful completion of the campaign.

One of the standout features of the Flipper Zero is its user interface, which embodies a pixel-art dolphin virtual pet. This game mechanic enhances the device's interactivity, as the usage of its functions directly affects the appearance and emotions of the virtual pet.

![](/posts/flipper-zero/flipper.png)

The Flipper Zero boasts various tools, including the ability to scan and replay sub-GHz frequencies, support for 125 kHz RFID, NFC, infrared, GPIO, iButton, Bad USB, U2F, and more. With such a diverse range of capabilities integrated into one device, the Flipper Zero enables users to effectively practice penetration testing and engage in other cyber security endeavors.

# Different Features

This multi-tool platform that allows you to run a variety of security tools and utilities, such as WiFi scanning and cracking, password cracking, and data analysis. The device has a small form factor and can be easily carried in your pocket, making it convenient for use in field work or on-the-go security assessments.

1. Wifi Scanning & Cracking:

    Flipper Zero boasts built-in functionality for wireless network scanning and cracking. With the ability to detect and identify WiFi networks, the device is capable of executing multiple attack methods for password penetration, including WPA/WPA2 cracking and handshake capturing.

2. Password Cracking:

    The device is equipped with password cracking tools, such as John the Ripper and Hashcat, to perform offline password cracking attacks. This makes it possible to crack encrypted passwords from various sources, such as Windows SAM databases and password hashes.

    To learn more about Password Cracking take a look at this blog post: https://medium.com/@joemcfarland/stealing-passwords-with-the-flipper-zero-1e05f3861648

3. Data Analysis: 

    Flipper Zero includes tools for data analysis, such as the Sleuth Kit and Autopsy, to help you perform digital forensics and investigations. These tools allow you to analyze hard drives, memory dumps, and other types of data storage to extract information and identify security vulnerabilities.

4. Portable & Customizable: 

    Flipper Zero is small and compact, making it easy to carry and use in various environments. Additionally, it runs a custom Linux distribution that provides you with complete control over the device and its configuration. This allows you to install and run your own tools and utilities, or modify the existing ones to suit your specific needs.

5. BadUSB:

    BadUSB is a security vulnerability that allows attackers to manipulate USB devices to perform malicious actions. The Flipper Zero has a built-in BadUSB feature that allows you to create malicious USB devices, such as rubber ducky or Hak5 LAN Turtle, to automate the execution of payloads and perform various types of attacks. This can be useful for penetration testing and social engineering exercises.

6. Sub-GHz:

    Sub-GHz is a frequency band that operates in the range of below 1 GHz. The Flipper Zero has a built-in Sub-GHz radio that can be used to communicate with other devices in the same frequency band. This allows you to establish wireless communication with other devices, such as sensors or actuators, and interact with them remotely. This can be useful for IoT (Internet of Things) security assessments and for exploring new attack vectors in the IoT space.

7. GPIO Interface: 

    The Flipper Zero is a multi-functional device that not only allows for interaction with access control systems, but also has the ability to connect to various components and devices through its General Purpose Input/Output (GPIO) interface. This feature provides users with the flexibility to extend the capabilities of the device, enabling them to utilize sensors, actuators, and other components to enhance their experience. With the ability to connect to these external devices, the Flipper Zero can provide users with a more comprehensive understanding of physical security systems and cyber security as a whole. Whether you are looking to practice penetration testing, carry out security assessments, or simply explore the world of cyber security, the Flipper Zero's GPIO interface is a valuable tool that offers endless possibilities.

8. iButton Support: 

    The Flipper Zero is equipped with iButton support, providing users with the ability to interact with and manipulate digital keys used in access control systems. iButton, also known as the Dallas Key, is a robust and secure technology that uses a small, stainless steel button to store digital information and perform various tasks, such as granting access to restricted areas or recording attendance. With the Flipper Zero's support for iButton, users can read, copy, and emulate these digital keys, making it a versatile tool for those interested in physical security and access control systems.

9. Infrared Support: 

    The device supports Infrared, which can be used for a wide range of purposes, including remote control, device synchronization, and more.

# Use Case

Overall, one example could be using the device to read and copy the RFID signals of an access card to gain unauthorized access to a building or restricted area. Another example could be using the GPIO interface to connect sensors and actuators for physical security assessments and penetration testing. The iButton support can also be utilized to crack digital access keys and unlock doors. Additionally, the device's ability to scan and replay sub-GHz frequencies and infrared signals can be used for wireless reconnaissance and eavesdropping. The U2F and NFC support can also be used for testing the security of these protocols.

Another possible use case for the Flipper Zero's Bad USB functionality is as a penetration testing tool for discovering security vulnerabilities in a target system. By emulating a malicious USB device, a security researcher can test the system's defenses and determine if it is vulnerable to Bad USB attacks. This information can then be used to recommend and implement appropriate security measures to protect against real-world threats.

Discover the capabilities of the Flipper Zero with this curated compilation video on "Flipper Zero in Public" available on YouTube. Explore how the device can be utilized in real-world scenarios by clicking the link: https://www.youtube.com/watch?v=UQC4yKrLN7U.

# Additional Features

The Flipper Zero has a range of capabilities straight out-of-the-box, but it can do even more with the addition of custom plugins and applications created by developers. You can also develop your own tools or plugins that build upon the existing features, allowing you to tailor the device to meet your unique needs and requirements.

Discover more potential with the Flipper Zero by exploring the 'Awesome Flipper Zero' GitHub repository. This comprehensive resource features a list of databases, dumps, applications, and plugins that can be used with the device. For even more functionality, consider installing a custom firmware like RogueMaster or Unleashed. This website provides valuable information and resources to maximize the use of your Flipper Zero.

Check out the repository at: https://github.com/djsime1/awesome-flipperzero.

![Alt text](/posts/flipper-zero/unleashed.png)

This tool is a must-have for anyone looking to expand their knowledge of cybersecurity and physical security tools. Its versatility, portability, and array of features make it a valuable asset for both beginners and experienced professionals.

This is the site where you can find the docs and where to buy it if your interested!

Flipper Zero: https://flipperzero.one/