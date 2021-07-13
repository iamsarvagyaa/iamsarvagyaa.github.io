---
title: "Think outside the box with Kunwar Atul"
author : Sarvagya Sagar
excerpt_separator: "<!--more-->"
image:
    path: /images/ama-session/04.png
    thumbnail: /images/ama-session/04.png
categories:
    - Interview
tags: 
    - AMA Session
---

Hey, everyone. After long time, I'm back with another interview with Kunwar Atul. He is an Application Security Engineer, have keen interest in DevSecOps, Mobile Security, and WebApp Security. Apart from these, He is an active member of Defcon, Null and OWASP. He worked on various applications with different different companies. Last year he gave a talk "Building Security Champions in Organization" in The Hack Summit. Without wasting more time, Let's get started ...

<!--more-->

- [How did you started and What got you into hacking?](#first-question)
- [Your methodology and workflow?](#second-question)
- [Your approach to learning new things?](#third-question)
- [How you manage your mental health, and burnout?](#fourth-question)
- [What is the biggest bug you found in your career?](#fifth-question)
- [How to find new areas of research like James Kettle did?](#sixth-question)
- [Throw some light on Mobile Hacking!](#seventh-question)
- [Which bug you love most and why?](#eighth-question)
- [At last, what you want to say to fellow peeps?](#ninth-question)

<a name="first-question"></a>
### :round_pushpin: How did you started and What got you into hacking?

From the early stage of my life I was not fascinated with tech, it all come suddenly. As I was preparing for NDA and cleared my exams, got a training letter and then my mom refused me to go. Then I started again figuring out what should I do in the future, because till 12th class I didn't even touch computers while my friends were learning computer basics, some were doing other courses related to computers. So I used to read lots of comics till 10th class and at that time I read Hacking word first time in my life. It was an article by Ankit Fadia yes Ankit Fadia and at that time I just imagined how intelligent these hackers are and of course, at that time I wasn't aware the reason behind his leetness 😜. Since that time hacking word was in my mind but I never thought one day I'll be in this field. Then somehow I told my brother that I want to learn Hacking and one of his friends suggest joining Facebook because at that time there were many hacking groups available on Facebook and from there I met Sanket Mhatre (cryptednanomet), I got the courage and I pinged him, he replied and I told him that I wanted to learn to hack and then he started guiding me. Meanwhile, I joined an institute for learning PHP, JAVA, etc. Once I asked one of my mentors that I wanted to become a Hacker and he laughed at me, said you can't be a Hacker because Hackers are extremely intelligent people and you are nothing in front of them, so stopped dreaming and focus on typing skills so you can get an operator job. My friends also laughed at me, they used to troll me even for choosing the IT field. Between all these struggles how can I forgot to mention Sourabh Sir, as he was the second person after my Brother to believe in me, he used to give me his laptop so I can read and do practical things, I used to write lot's of batch scripts for deleting files, formatting C drive and crashing computers/laptops, etc.

Then I met Jay Jani (JayJani007) he also helped me to understand concepts of web pentesting. Then I met some other people on social media like Parth Malhotra (Parth_Malhotra), Sujit Ugale, Sandeep (geekboy), Sri Ram, etc. 

I got my first job as a Trainer in Appin, and I used to sleep in the office only because of free wifi. I used to spent my whole night learning new stuff, doing practicals and all. Now I completed 6 official years in Infosec domains, met so many people in India and across world and got network between all of them. Now so many youngsters are in the Infosec domain with excellent skills and they always motivate me to learn and grow in this field.

<a name="second-question"></a>
### :round_pushpin: Your methodology and workflow?

Before starting pentest any application, I first read the documentation which gives a lot of information regarding the application, and then I use the application as a normal user, I try to understand the workflow of the application. 

For Android - start with Static analysis, like first I do a scan with MobSF and check what all issues have been identified, and then with the help of Apktool, I reverse the application and look for hardcoded sensitive information in the application like username, passwords, API keys, any internal URLs, etc. I also look into firebase URL to check whether it is badly configured or not, Broken TLS, Broken Cryptography, etc. I also read smali codes to understand the registers and values what's going on behind the application and How the application is running. Then with the help of Drozer, I look for exploitable activities, content providers, broadcast receivers, etc, also I look at shared preferences, insecure WebView, dead code, SQLite database, insecure logging, keyboard caching, etc. 

For iOS - start with MobSF for static analysis and then look for other issues like keyboard caching, Info.plist for sensitive data, NSUserDefaults, SQLite database, cookies inside the app folder, cache, snapshots, data in the keychain, logs, broken cryptography, etc. Later I start with Dynamic analysis as per community standards.

<a name="third-question"></a>
### :round_pushpin: Your approach to learning new things?

Google is your best friend, and I always keep an eye on Twitter, Facebook Groups, Linked In (sometimes), StackOverflow. I follow a lot of young people from Infosec Domain who share lots of learning material on Twitter, so I use to bookmark all those important tweets and in free time I use to read those articles, blogs, research paper, etc.

<a name="fourth-question"></a>
### :round_pushpin: How you manage your mental health, and burnout?

Basically, I always took small breaks while doing office work or my own studies. I talk with family, love to spend time with them, during weekends I watch movies, anime, read about the history of Rajputs, old songs always work for me, going out with friends, having chai, coffee with them, traveling all these help me to recover from burnout and mental health.

<a name="fifth-question"></a>
### ### :round_pushpin: What is the biggest bug you found in your career?

It all depends on engagement to engagement there are a few like SQL to RCE, RCE in Jenkins instance, etc. But I have an interesting story related to one of client engagement. So that client used to get Compliant report in every quarter and when I joined the Org, they gave me their application to pentest. I spent 2 days with nothing and then I got a call from a client, he asked me to release the report as compliant. I said without testing how can I release the complaint report and it is just 3rd day of engagement. He said we have fixed all the issues and you will get nothing.

So I thought to look into all the old reports and I observed a SQL injection vulnerability which was fixed. I thought to bypass the SQL injection validations and I started looking into it. Luckily I got the insertion point and from there I got all the database information and from there I escalated it to RCE.

<a name="sixth-question"></a>
### :round_pushpin: How to find new areas of research like James Kettle did?

He is an awesome person and I can not compare myself with him. But yes I always look for some new and trending topics in domain, then I look for resources like blogs, papers etc and in free time I prefer to read those collected resources. If you have the curiosity to learn something you will do it simply. 

<a name="seventh-question"></a>
### :round_pushpin: Throw some light on Mobile Hacking!

Mobile Applications have become an important part of our lives as our dependence on smartphones has grown. But many users are unaware of the security of their devices. Organizations can avoid the risk by pentesting the mobile applications on a time to time basis. There are different types of Mobile Applications - 

- **Native apps** - are created for one specific platform or operating system.
- **Web apps** - are responsive versions of websites that can work on any mobile device or OS because they’re delivered using a mobile browser.
- **Hybrid apps -** are combinations of both native and web apps, but wrapped within a native app, giving it the ability to have its own icon or be downloaded from an app store.

**Android Applications -** An Android app is a software application running on the Android platform. Because the Android platform is built for mobile devices, a typical Android app is designed for a smartphone or a tablet PC running on the Android OS.

Android apps are written in the Java programming language and use Java core libraries. They are first compiled to Dalvik executables to run on the Dalvik virtual machine, which is a virtual machine specially designed for mobile devices. (Definitions from Techopedia)

**iOS Applications -** IOS is a mobile operating system for Apple-manufactured devices. iOS runs on the iPhone, iPad, iPod Touch, and Apple TV.

iOS is derived from Mac OS X and is a Unix-like OS. There are four abstraction layers within iOS:

- Core OS Layer: Provides low-level features as well as frameworks for security and interaction with external hardware
- Core Services Layer: Provides services required by upper layers
- Media Layer: Provides the necessary technologies for graphics, audio and video.
- Coca Touch Layer: Where frameworks are located, which are often used when creating an application

iOS comes with a lot of default apps, including an email client, a Safari Web browser, a portable media player (iPod), and the phone app. (Definitions from Techopedia) 

**Mobile App Penetration Testing Methodology -**

**Reconnaissance -** It is possible to find out information related to target applications using search engines, third-party libraries, source code repositories, developer forums, etc. The better you understand the application, the more chances are getting crucial vulnerabilities.

**Assessment -** Mobile applications have a unique way to test, a pentester should check the application pre and post-installation. This can be achieved by static analysis without installing the application, on the decompiled source code and accompanying files, dynamic analysis can be achieved by running the application means during runtime we can achieve dynamic analysis. Reverse engineering could be attempted to convert the compiled applications into human-readable format.

**Exploitation -** To demonstrate a real-world data breach, a properly executed exploitation can happen very quickly. This involves

- **Attempt to exploit the vulnerability -** Acting upon the discovered vulnerabilities to gain sensitive information or perform malicious activities.
- **Privilege escalation -** Demonstration of identified vulnerability to gain privileges and attempt to become a superuser.

**Reporting -** This involves creating a detailed report about the discovered vulnerabilities, including the overall risk rating, description, the technical risk associated, technical impact, the business impact and proof of concept, and recommendations to fix the findings.

Tools that can come in handy - 

- APKAnalyser
- Drozer
- APKTool
- dex2jar
- JD-GUI
- Androguard
- JDB debugging

The Different tools which can be used for iOS Pen test are

- oTool
- keychain dumper
- LLDB remote debugging
- Clutch,
- Class-dump-z
- Instrumentation with Frida
- Cycript
- Hopper
- Snoop-it

<a name="eighth-question"></a>
### :round_pushpin: Which bug you love most and why?

The bug which I love most is IDOR, XSS  because it is easy to find, SSRF and mostly I focus on logical vulnerabilities.

<a name="ninth-question"></a>

### :round_pushpin: At last, what you want to say to fellow peeps?

- **Don't let people fool you in the name of Cyber Security/Bug Bounty Courses.**
- Always follow your stint and remember never to compare yourself to others, always try to be a better version of yourself.
- See failure as a beginning and part of the process
- There are lots of resources available in Google, just type your query and you shall get a bunch of resources.
- Patience is key to success
- Be kind to others
- Apply learn-By-Doing Methodology

Believe in yourself, your learning, and stay humble. It will help you to grow in the Infosec community. Also, take care of your mental health, talk to your family and friends if you are having any issues.

#### Contact

- LinkedIn - [https://linkedin.com/in/kunwaratulhax0r](https://linkedin.com/in/kunwaratulhax0r)
- Twitter - [https://twitter.com/kunwaratulhax0r](https://twitter.com/kunwaratulhax0r)

<center><b>I'm on <a href="https://www.buymeacoffee.com/iamsarvagyaa" target=_blank>buymeacoffee</a>, you can join with me on buymeacoffee 😄</b></center>
