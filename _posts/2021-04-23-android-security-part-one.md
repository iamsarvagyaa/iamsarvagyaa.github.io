---
title: "Diving in Android Security"
author: Sarvagya Sagar
excerpt_separator: "<!--more-->"
image:
    path: /images/android-security/hero-thumbnail.png
    thumbnail: /images/android-security/hero-thumbnail.png
categories:
    - Android Security
tags:
    - Android
    - Beginner 
    - Pentesting
---

Hello everyone, This is my first blog post. Many of my friends suggested me to get into *Android Security*. I started learning android security and learned many things, but I faced a lot of problems. So I wanted to create a series of blog posts to guide those peeps who wanna get into android security. You know what? There are fewer resources about android security on the Internet. This article will explain some android internals, which helps us to understand the android architecture. I'm a complete newbie in android security, So pardon me if there any mistake in this article, or you can correct me if there's any mistake in this article.

<!--more-->

:bulb: I will not show you how to install and set up an Android pentesting lab. Rather, I will tell you some good tools to help you with the pentesting Android application...
{: .notice--success}

There are no prerequisites to learn android pentesting, but if you know android development and have a good understanding of How the web and internet works, this will help you. By the way, I will try to explain more simply and easily. I hope you will learn something. 🙂 Basically, the android operating system is a **Linux-based operating system** platform, which Google developed. Nowadays, the android is a foundation of many devices like android phones, smartwatches, smart TVs, and many more things that work on the Android operating system. That's why I'm saying android application security is in high demand because we all know that most companies are shifting their whole business to mobile applications. So, we have more chances to get paid in android-security. This small blog post will describe android fundamentals. First of all, I'm going to introduce the structure of this android series ...

-   Android's Architecture
-   Android components and android apk structure in detail.
-   How android applications are built and run.
-   Reading and Understanding of smali code.
-   Understanding AndroidManifest file in detail.
-   Tools Intro - Tools that will give you supernatural powers.
-   Information Gathering, Methodologies, and Workflows.
-   Static analysis vs. Dynamic analysis.
-   Reversing Android applications for fun and profit.
-   Walkthroughs of vulnerable android applications like `InjuredAndroid`, `DIVA`, `mstg-crackme`, etc.  

These are upcoming blog posts. Well, I don't know much more about android application security. I planned this series to help others and for myself too. I will also write a detailed blog post about Automating your workflow in android pentesting. Now, I'm going to cover *Android's architecture*.

## Android's Architecture

Android app can be written in Java, Kotlin, and C++, but nowadays, there are many frameworks available to create android applications. One of the most popular frameworks is Flutter. Their lot of android applications are developed in a flutter. **Android SDK** compiles your source code and the manifest, data, and resources files into an archived android package with `.apk` extension. Android applications don't have direct access to hardware resources, and each app lives in its own security sandbox. By default, each application has access to the components required to do its work. Android system implements the principle of least privileges. *This will create a very secure environment in which the app can't communicate with other parts of the android system without permission*. We will learn more about permissions and application sandboxing features in the next blog post. Now, let's understand the essential part, the architecture of the android application. 

The architecture of the Android stack consists of *pre-installed applications, native libraries, android Application Interface (API) frameworks, Android Runtime (ART), Hardware Abstraction Layer (HAL), and Linux kernel*. Now, understand one by one what are the uses and work of these layers.

![Android Architecture]({{ '/images/android-security/android-archit.jpg' }}){: .align-center} 

Starting from the bottom layer, which is the **Linux kernel**. We can say the Linux kernel is the heart of the android operating system. If you're from a UNIX background, you will know that the kernel provides drivers for hardware and core services like memory management, process management, and file system access. On top of the kernel is the **Hardware Abstraction Layer** which acts as an abstraction between the android's physical hardware and its components. HAL consists of multiple library modules which implement an interface for a particular type of hardware component. When an API framework calls to access the hardware, the library module will load for the hardware component. For example, if an application wants to connect with the camera, it will allow an application to use a camera and sensor. Above HAL, there is native userspace which consists of `native libraries`, `native daemons` and `init binary`. Init binary is a process that starts other processes in Android. Native libraries are written in C/C++ core libraries and java libraries. These libraries get exposed to you through the API frameworks. Another side we have Android Runtime :heart:

**Android Runtime:** An alternative to the Dalvik Virtual Machine. After Android version 4.4, `Android Runtime (ART)` is introduced, which have major changes and features, and this change replaced the Dalvik VM. Specially, Android Runtime is written to run multiple machines by executing `DEX files`. After android version 4.4, each app runs into its own process and its own instance of the Android Runtime (ART). In the next upcoming post, we will learn in detail. Along with Android Runtime, there are also core java libraries that are important to run an application.

The top and upper part of Android's architecture is **API frameworks and pre-installed applications**. These APIs help you to reuse code of core modular system components. These API frameworks are written in java and consist of managers, content providers, view systems, etc. You can use these APIs to control what your app looks like and how it behaves. It provides a lot of classes and interfaces for android application development. At last, android comes with a pre-installed application such as calendar, Home, Contacts, etc.

There lot of things to learn in the basics of the Android security model, and I will try to explain them in a detailed way. We'll cover all the topics like the *permission model, privilege separation and sandboxing, Storage and database isolation, filesystem isolation, broadcast receivers, application booting process, application signing*, etc. Now, I'm going to tell you OWASP Mobile Top 10 in short because you'll get an overview of the present at-risk attacks.

- **Improper Platform Usage:** Attack covers misuse of platform features and improper platform security controls. Attack scenarios like leakage of Data via exploiting android intent, Sniffing of android intent, Poor web services authentication and configuration, etc.
- **Insecure Data Storage:** This attack is marked on the second number, attack scenarios like accessing internal files/logs if a mobile device is stolen, exploiting unsecured data, compromised file systems like SQL databases, sd cards, cookies stores, etc.
- **Insecure Communication:** Man in the Middle attack, Stealing information through insecure wifi-connection, and compromised radio-frequency related traffic can be marked as Insecure Communication.
- **Insecure Authentication:** Typically, exploitation of authentication is automated through many tools or self-build tools. Scenarios like exploitation of Input form and hidden service requests are in this vulnerability.
- **Insufficient Cryptography:** In most cases, developers use MD5, SHA1, RC2, MD4, etc., which causes stealing of user data easily, and also hackers can access insecure encrypted files.
- **Insecure Authorization:** Unauthenticated access to admin endpoints and panel, IDORS, etc related scenarios can covers this attack.
- **Poor Code Quality:** Exploitation of this attack is difficult; however, we can perform buffer overflow, client input bypassing, etc., like attacks.
- **Code Tampering:** An attacker can exploit code modification via malicious input fields of the apps hosted in third-party app stores. Phishing, Spreading of malware are in this attack vector.
- **Reverse Engineering:** Attackers can easily analyze the app's internals and link with server processes. Bypassing of premium features, Code stealing, etc., related scenarios are in Reverse Engineering.
- **Extraneous Functionality:** An attacker can download the app and can examine the log files, configuration files, can create logs to examine the errors, and can also pull stagging information. These scenarios are in Extraneous Functionality, and this is the last attack of OWASP Mobile.

One of thing more, this will take time because I have less time to write a blog post. In the next post, we will learn about android components and the structure of android applications in detail. Thank you for reading this small blog post, and I hope you learned something from this :handshake:

<center><b>I'm on <a href="https://www.buymeacoffee.com/iamsarvagyaa" target=_blank>buymeacoffee</a>, you can join with me on buymeacoffee :smile:</b></center>
