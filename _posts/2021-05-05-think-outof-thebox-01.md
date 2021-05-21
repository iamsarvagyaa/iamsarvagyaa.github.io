---
title: "Think outside the box with Debangshu Kundu"
author : Sarvagya Sagar
excerpt_separator: "<!--more-->"
image:
    path: /images/ama-session/01.png
    thumbnail: /images/ama-session/01.png
categories:
    - Interview
tags:
    - AEM Security
    - Bug Bounty 
    - API Security
    - AMA Session
---

I'm back again with a new series of posts named "Think outside the box," inspired by [PentesterLand's AMA](https://pentester.land/ama). I planned to interview good hackers, where I asked a few questions about his industry domains. This is the first post in this series of interviews, and I'm pleased about this initiative. So, today I'm going to invite a young bug-bounty hunter "Debangshu Kundu." He is a seeker of knowledge, and I learned a lot from him in the past 3months; that's why I want to invite him as my first guest. He gave me wonderful replies to all the questions which I asked him. Thank You, so much Debangshu bro! :heart: for all the well-explained answers. Let's start without wasting more time. We are going to dive deeper into a pool of exciting answers from Debangshu. Below are asked questions with table of contents, you can also use toc from here ...

<!--more-->

- [How did you started and What got you into hacking?](#first-question)
- [Your methodology and workflow to hunt bugs?](#second-question)
- [Your approach to learning new things?](#third-question)
- [How do I stay motivated after getting duplicates and N/A?](#fourth-question)
- [What advice do you want to give to all of us?](#fifth-question)
- [How you manage your mental health, and burnout?](#sixth-question)
- [Why you love AEM Security?](#seventh-question)
- [How to find new areas of research like James Kettle did?](#eighth-question)
- [Through some light on API Security!](#ninth-question)
- [At last, what you want to say something to fellow peeps?](#tenth-question)

![Debangshu Kundu]({{ '/images/ama-session/interview-01/dk999-bc.png' }}){: .align-center}

- Bugcrowd Profile - [https://bugcrowd.com/DK999](https://bugcrowd.com/DK999)
- Twitter - [https://twitter.com/debangshu_kundu/](https://twitter.com/debangshu_kundu/)
- LinkedIn - [https://www.linkedin.com/in/dk999/](https://www.linkedin.com/in/dk999/)

<a name="first-question"></a>
### :round_pushpin: How did you started and What got you into hacking?

I was fascinated with tech from an early age, and once I saw a *social engineering video on YouTube*, that got me intrigued about what hacking was! I searched more about it and found out about defacing. Back then, it was really cool! (I don't encourage it, but that's what I did initially), as days passed, I learned more about it and got addicted to hacking (websites). The whole idea of taking over accounts with 0/1 clicks, run arbitrary commands, leak sensitive data with a few clicks felt just like magic, and that was the driving factor!

<a name="second-question"></a>
### :round_pushpin: Your methodology and workflow to hunt bugs?

Initially, I start my recon process normally with *Subdomain Enumeration*, preferably from multiple tools to utilize maximum data sources. Be sure to add in the API keys (free ones) to maximize the data collection. Alternatively, I also do `DNS brute-forcing` and filter out the responding ones. Then, I grab the screenshots of all the subdomains and any other related domains. Followed by brute-forcing directories with :
- A generic wordlist
- Target/Technology specific wordlist

This way, I'm less prone to missing out on a juicy endpoint! Sure, it takes time, but it is worth it. Additionally, I grab all of the JS files and scrape for endpoints/interesting keywords that greatly aid my content discovery process. Also, I use custom CSE's that leverage multiple paste sites like Pastebin, Trello, Github, GitLab to enumerate and find information about the target I'm hacking on. Other than that, I use other search engines like `Shodan, Fofa, Censys to gather more intel via simple filters, viz title, hostname, SSL, and org`. Depending upon the type of target, If it's a web app with lots of functionalities and clear-cut documentation, that's my first go. Believe me; `there isn't a better way to understand the application flow! If it's a CMS-specific target, I'd study the CMS's documentation and publicly available exploit and resources to figure out how stuff works and how to get started breaking into them.`

I've found this approach to be quite rewarding and results in lesser duplicates. One can set it up locally and try to find vulnerabilities with a white box approach and replicate the same on a possible bounty target. Portswigger and the **WAHH handbook** is the best all-around resource you can get for free to a) read up on the latest research techniques and b) practice all sorts of vulnerabilities to gain a better understanding of them. Finally, a word of advice, use the Developer Tools of Chrome/Firefox, preferably the latter, to your fullest, you'll definitely thank me later!

<a name="third-question"></a>
### :round_pushpin: Your approach to learning new things?

First of all, I try to collect information from multiple sources to find an edge amongst them. **Google is your biggest friend**. Learn to use google dorks and other google search operators well. You don't need to be a master in everything from the right beginning; all you need to know how to **Google/Bing/StackOverflow** well. Take this with a grain of salt, of course. Next, prepare descriptive and structured notes of every topic you study or every functionality you encounter. If you can't do that, then at least try to make a notion, sublime text document, and throw in all the random stuff there for your future self to access and refer to them. Always read multiple sources, sometimes non-English sources too. I've often found invaluable information via non-English sources, e.g. Chinese articles, when there was only limited information on pure English sources. Also, it's necessary to experiment a lot if you want to be a better learner. `Please read up on some topics, try doing some labs, or even practice it live on bounty targets. Try and Fail! Try Again and Fail Better! You'll get to it sooner or later`, but you mustn't stop : 
- trying
- experimenting, and
- reading

I don't use any methodical or structured way to learn stuff. I read first then, get a hands-on approach, read more, and the cycle continues. This in no way has to be a balanced cycle but a continuous one. Lastly, ample rest is important too! Give importance to your mental health to avoid frequent burnouts because the best of bugs come when you're well focused!

<a name="fourth-question"></a>
### :round_pushpin: How to find bugs that are not duplicate, and How do I stay motivated after getting duplicates and N/A?

I tend to focus on a certain niche very much, say a specific CMS, deep dive into it, explore all of its documentation, dig into already available research, and formulate my attack strategy. As I mentioned earlier, I'd rather spend some time reading docs before starting my attack; this way, I'm more well acquainted with the application than others. Also, I'd try non-conventional methods like signing up for a webinar (I found a sweet bug doing that once) too! As everyone says, **a duplicate is a valid bug too!** If you spent hours on the bug and received a duplicate, congratulate yourself and try taking it positively; maybe try the same approach on a different target. Who knows, you might score one! But, if it's an easy/low-hanging fruit, there's nothing to whine about it; **try and hack better!**

Now, a word on Not-Applicable submissions, If you genuinely believe a bug has an impact, and it gets closed unfairly, be sure to resubmit the bug, maybe include some extra details to rectify any/all mistakes in the original submission. This may give your submission another chance to be looked at. Alternative options include informing Support and having them have a look at it. `Let's face it, your submissions won't face justice 100% of the time, but you have to keep going, maybe switch the programs, but never let that one N/A deter you.`

<a name="fifth-question"></a>
### :round_pushpin: What advice do you want to give to all of us?

Keep your basics strong, experiment a lot. Stick to one program for the long run (preferably wild scope), pick up a niche, take ample breaks, study new stuff, keep yourself updated with the latest research, read documentation, try all the crazy stuff out! Don't be afraid to come out of your comfort zone to grow and evolve. Stay indoors and wear masks while going out.

<a name="sixth-question"></a>
### :round_pushpin: How you manage your mental health, and burnout?

Sigh! Mental Health can be hugely overlooked in these times. Please don't do that. I tend to divide my day into 3 parts (roughly). First, I dedicate myself to studying and learning about new stuff, Second to working on something, and the Third part to resting. These are in no particular order or distributed equally. Drink ample water, which boosts brain performance. There will be days when I don't want to hack/learn stuff, and that's okay. Give yourself room, maybe partially automate your workflow to get some checks done. Burnouts may happen to you someday, and it's alright! It would be best if you worked through it. Go for a walk (with necessary precautions), ride your bicycle (with necessary precautions), play your favorite game, watch any good movie, basically do stuff you love! And then slowly pick up things. Procrastination, I used to struggle a lot with it, maybe planning your day in advance, as I said earlier, may help! It worked for me, might/might not work for you. Avoid sitting idle. Keep yourself engaged positively. That's all.

<a name="seventh-question"></a>
### :round_pushpin: Why you love AEM Security?

First of all, this is an area that most hunters overlooked, so there are lesser chances of duplicates and more potential to find really unique and interesting vulnerabilities that no one cares to look for. You can find `XSS (Cross-Site Scripting), SSRFs (Server Side Request Forgery), RCE (Remote Code Execution), and tonnes of access control issues`. Sure, you have to spend hours looking through the docs to find something of interest, something that has no existence in the public domain/ already available/disclosed research. A thing about AEM is, it is a combination of multiple technologies like Java, Apache Sling, Apache Felix, etc. Apache Sling is open-source, so finding an access-control bypass there would mean you could possibly use it in AEM targets too! There's a lot of room here to explore and experiment with; that's what I love the most about AEM. Getting started, all the research work of **Mikhail Egorov** [https://speakerdeck.com/0ang3el](https://speakerdeck.com/0ang3el) on Adobe Experience Manager, **Frans Rosen's** beautiful talk, [https://speakerdeck.com/fransrosen/a-story-of-the-passive-aggressive-sysadmin-of-aem](https://speakerdeck.com/fransrosen/a-story-of-the-passive-aggressive-sysadmin-of-aem) were beneficial. Apart from that, my go-to reference is AEM Documentation. Also, last but not least, a big thank you to [@AemSecurity](https://twitter.com/AEMSecurity) for the constant support!

<center><blockquote class="twitter-tweet"><p lang="ja" dir="ltr">⠀ (\__/) <br>   ⠀ (•ㅅ•) <a href="https://twitter.com/AEMSecurity?ref_src=twsrc%5Etfw">@AemSecurity</a> finding AEM 0day <br>　＿ノ ヽ ノ＼ __ @ everywhere<br> /　`/ ⌒Ｙ⌒ Ｙ　ヽ <br>( 　(三ヽ人　 /　　 | <br>|　ﾉ⌒＼ ￣￣ヽ　 ノ    <br>ヽ＿＿＿＞､＿＿_／ <br>　　 ｜( 王 ﾉ〈 (\__/) <br>　　 /ﾐ`ー―彡\ (•ㅅ•) me finding GETservlet</p>&mdash; DK999 (@debangshu_kundu) <a href="https://twitter.com/debangshu_kundu/status/1366079518495145996?ref_src=twsrc%5Etfw">February 28, 2021</a></blockquote></center> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script><br>

<a name="eighth-question"></a>
### :round_pushpin: How to find new areas of research like James Kettle did?

Woah, I feel like I'm not capable enough of answering this question. All I can say is, while doing content discovery on some target X, if you find some random CMS or technology that's not very common, feel free to dig into the available documentation and, if possible, build a local instance of the same. Once you find a bug, try scaling it internet-wide on any/all bounty targets, profits ++. There's no sure-shot way of going down this path, but if you pick up a niche and be persistent towards it, I'm sure you'll definitely have some success.

<a name="ninth-question"></a>
### :round_pushpin: Throw some light on API Security!

Talking about API Security, it's a very vast topic, and a wide one too. There are various implementations, ranging from websites to mobile apps to IoT Devices and whatnot, although the core idea remains the same. There's a lot of Access Control Issues and Authorization Based issues to be found here. Depending upon the type of API you're testing, there will be a different workflow, say, some function X parses XML file with the Content-Type `application/xml`, try including external entities in the request to check for **XXE**. If it's Ruby-On-Rails, try appending .json to certain endpoints to bypass certain checks or **leak PII**. If It's Oauth, check for various things like redirect_uri, state parameter, validate the assigned scope of the application in use. If it's a REST API with Content-Type `application/json` apart from all the already known basic attack techniques like **XSS, CSRF, and its bypasses, IDOR**, also take a look at the beautiful research by BishopFox here, [https://labs.bishopfox.com/tech-blog/an-exploration-of-json-interoperability-vulnerabilities](https://labs.bishopfox.com/tech-blog/an-exploration-of-json-interoperability-vulnerabilities). You can use this as a reference/how-to approach JSON APIs. If it's JSON, you can't ignore JWT's too, there are lots of checklists regarding the same, feel free to google them. Then, there's **graphql!** There are already tonnes of public h1 reports you can find with a simple dork, `site:hackerone.com "graphql"`.
Also, yet again, for the zillionth time, read the docs! If you're testing an API, and there's public documentation, there can't be a better resource than studying the target application. Also, there are many companies using 3rd Party APIs, too, that could be an absolute goldmine with existing misconfiguration, i.e. (vulnerabilities arising due to faulty implementations), a good example of such an access control issue is Salesforce Aura API. There's a good blog detailing the same, find it here: [https://www.enumerated.de/index/salesforce](https://www.enumerated.de/index/salesforce). An excellent all-round resource is **API Security 101 by Sadako**, here: [https://pentester.land/conference-notes/2019/03/08/levelup-2019-api-security-101.html](https://pentester.land/conference-notes/2019/03/08/levelup-2019-api-security-101.html)

<a name="tenth-question"></a>
### :round_pushpin: At last, what you want to say something to fellow peeps?

Be persistent, take care of your mental health. Enjoy what you do. Explore lots! Keep Experimenting, Learn the basics well, Read Docs, stay indoors and wear a mask while going out!

<center><b>I'm on <a href="https://www.buymeacoffee.com/iamsarvagyaa" target=_blank>buymeacoffee</a>, you can join with me on buymeacoffee :smile:</b></center>