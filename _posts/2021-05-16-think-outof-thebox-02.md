---
title: "Think outside the box with Satyam Gothi"
author : Sarvagya Sagar
excerpt_separator: "<!--more-->"
image:
    path: /images/ama-session/02.png
    thumbnail: /images/ama-session/02.png
categories:
    - Interview
tags:
    - Bug Bounty 
    - API Security
    - AMA Session
---

Hey, all. I hope you all are well during this pandemic. First of all, I would like to thank all of you for loving the interview sessions. I got a wonderful response in the last interview. Today, I'm going to invite "Satyam Gothi aka RogueSMG". He is a security analyst in *Securelayer7*, a bug bounty hunter, and also a content creator. I fell in love with his videos and How he breaks down all the things. Kudos to all the efforts. Thank You, so much Satyam Gothi! :heart: for all the well-explained answers and also for creating contents. In future, We want more contents from you. I request everyone to subscribe his channel. This is the second post in series of Interviews. Let's get started!

<!--more-->

- [How did you started and What got you into hacking?](#first-question)
- [Your methodology and workflow to hunt bugs?](#second-question)
- [Your approach to learning new things?](#third-question)
- [How do I stay motivated after getting duplicates and N/A?](#fourth-question)
- [What advice do you want to give to all of us?](#fifth-question)
- [How you manage your mental health, and burnout?](#sixth-question)
- [Which domain you love most in security industry and why?](#seventh-question)
- [How to find new areas of research like James Kettle did?](#eighth-question)
- [Through some light on Android Security!](#ninth-question)
- [At last, what you want to say something to fellow peeps?](#tenth-question)

![Satyam Gothi]({{ '/images/ama-session/interview-02/rogue-yt.png' }}){: .align-center}

-   Youtube Channel - [https://www.youtube.com/c/RogueSMG/](https://www.youtube.com/c/RogueSMG/)
-   Twitter Handler - [https://twitter.com/RogueSMG](https://twitter.com/RogueSMG)
-   LinkedIn - [https://www.linkedin.com/in/satyam-gothi](https://www.linkedin.com/in/satyam-gothi)

<a name="first-question"></a>
### :round_pushpin: How did you started and What got you into hacking?

Since my childhood, I was always more excited about taking things apart, like toys or electronics, to try and understand what was going on inside. Though I rarely actually understood what was going on but it just gave me a Dopamine hit. Fast forward a few years later, and by God's grace, I was quite lucky enough to have access to a laptop not so late. A friend of mine had got a brand new iPhone 3gs. And that phase was all about, you know, cracking PSPs, jailbreaking the iPhone `(trust me, that feeling was unparalleled to know Cydia has pretty much everything)`, rooting some Android phone to mess around with all the freaky customizations, making Phishing websites `(it took around 3-4 days for the hosting to realize it and take it down)` and just firing Kali stuff on the local network to change Images and snoop traffic, etc. 

I only had an idea of **"how"** but never anything about the **"why" & "what"** of these. It was all just out of curiosity and to look **"cool"** :P. So at this point, I was already clear of what career path I'm gonna choose when the time comes and that I did. I pursued my Bachelors in Computer Engineering, and just then, after being done with it, back in after 2019, I actually started to see and understand the **"Why" & "How"** of things, infosec. And sure, making the same mistake people do, I joined a local "Ethical Hacking" certification course which pretty much was useless. And though I didn't immediately act upon it, but there is where I first came to know about Bug bounties. Just last year in 2020, after some intense few months, I landed my first Infosec job. And there I met one of my colleagues, who's a pretty good friend now. He's the one who actually guided and helped me get started into BB. Quite a hefty portion of everything I know & do today, tech or non-tech, thanks to him [(@dark_warlord14)](https://twitter.com/dark_warlord14).

<a name="second-question"></a>
### :round_pushpin: Your methodology and workflow to hunt bugs?

Initially, just like everyone I asked around, I googled around and started with **OWASP top 10**. As I moved on and realized Twitter had an insanely good Infosec community, I started looking and following everyone who seemed associated with BB or Infosec in some way. And then Recon came into the Picture. Recon was everywhere, `Portswigger had few Labs, Nahamsec didn't yet have a Twitch, Bugbountynotes was still alive, ProjectDiscovery wasn't into existence`. I devoted quite a good amount of time to learning & understanding different ways & techniques of Recon and got into Automation. But the more I looked into it, the more I realized that there's an absolutely crazy amount of stuff into it which I didn't even consider. I was quite reliant on Recon for some time, but then I felt that I was either too bored or exhausted by the time I actually have to process and act upon the recon data. **[Zseano](https://twitter.com/zseano)**, an amazing hacker and an even better person, consistently used to post and thanking people for getting so busy with Recon and leaving the main App fresh & quite untouched for him to pwn. I guess I felt it but didn't act upon it until much later xD. Finally, I decided to put a hold on extensive Recon now and focus rather on diving deep into the application.

So my workflow nowadays is just basic recon: `Subs, Ports, Alive/Web domains, httpx/httprobe, Grab status code, title, server`, and manually look through it. While all this is happening, I simultaneously do some Google Dorking and look around into Shodan. If I find something uncommon or interesting, I'll usually start with Dir Brute on that domain. The only automation I do apart from the above is looking for easy **SQLi/XSS** or so from **Waybackdata/gau**, nothing crazy. But that rarely has any success tbh, because it's something that almost everyone else is doing. And Nuclei is also something I use very rarely, if at all. I'll then Pick a sub, fire up burp, sign up 2-3 accounts and start diving into that. In the 1st iteration, I identify the technologies being used and try to move through the app, `blindly firing basic payloads for Injection related vulns, look for csrf, cors, etc.`, JWT related issues if being used, exploits specific to that Server or tech, and all that stuff which I can think of trying without needing to understand what the web app does & how. 

In the 2nd iteration, I normally try to traverse the web app, proxying everything through burp, trying to understand what it is all about and how it functions. And finally, in the 3rd iteration, I'll pick up a particular functionality or module. Let's say dashboard and try to find whatever I can from **BAC to Business Logic** stuff, whatever's relevant in that scenario.

<a name="third-question"></a>
### :round_pushpin: Your approach to learning new things?

Google, Twitter, Medium, Github, Youtube, There's a humongous amount of resources available. If you're curious and desperate enough, you'll almost certainly find whatever you're looking for. And of course, there's a lot of amazing people out there you can reach out for help with anything. But please don't ask, `"How to get started to how to exploit XYZ?"`. Google it, do some research and then finally, if you're unable to understand any particular thing, ask that thing precisely, Eg. "I read a blog on JWT, and it says this is how it should behave if it has issues. But this is how it's behaving in my case, it's not normal as far as I can tell, but I can't seem to understand or exploit it; can you please point me in the right direction?"

<a name="fourth-question"></a>
### :round_pushpin: How do I stay motivated after getting duplicates and N/A?

First of all, I honestly haven't been hunting as much as I should. Managing a Full-time job, Youtube, Hunting, learning new stuff, all while being home 24*7 has been quite hard `(I've finally made some pretty significant changes for that, so let's see how it goes now)`. Secondly, I don't have many N/As or Dupes as I don't look for/report Low hangs. I only do that if I've been trying to find something for, let's say, 5+ hours constantly or after 2-3 days, and I am desperate enough to submit a Report. But even while writing the Report, I kind of know it's gonna be a **Dupe/Informative**, so I pretty much don't expect anything, and it's just for myself to not feel like I haven't been productive or so. Another scenario, while I might throw in Low hangs, is if I'm trying to hunt on a VDP. I'd rather invest my time creating Bug Chains to find high-impact stuff on a BBP rather than banging my head around for a HOF or T-shirt.

<a name="fifth-question"></a>
### :round_pushpin: What advice do you want to give to all of us?

Don't compare yourself to others, Be curious and stop hunting just for the Money. It could be hard for the ones doing it full-time, but for the rest of almost everyone doing it part-time, you should approach it as a way to keep yourself engaged and improve yourself all while having some fun. If you learn to drive a car, you don't just start to see all other cars on the road as your competitors and attempt to race through them and Win. There's no common Finish Line; everyone will head down their own different routes. And even you reaching to your destination eventually is inevitable. So slow down the speed, turn on the Radio and enjoy the Journey!

<a name="sixth-question"></a>
### :round_pushpin: How you manage your mental health, and burnout?

Shut down the Laptop and get away from the Screen. I am someone who cannot stay home or at a single place all the time and keep working. I need to get out to clear my Brain. But I can't go out for now (at least in India), so I spend more time with my family. These are fucked up times, no doubt. But on the other hand, you probably will never get so much time to spend with your family. So cherish every moment, make some memories and tell them how much they mean to you and how much you love them. After that, I can't avoid my Day job, so maybe I'll work on making Videos for Youtube or watching a movie/reading some book, or just not opening my Laptop altogether. And I don't define my "Off time" by the number of days. Since nothing else I can do for now and I can't go out, it sometimes takes more time for me to get back up and pumping. So I might stay away from doing much for maybe 2 days or 10 days, depending on how burned out I am. Remember, the healthier you are, both mentally and physically, the better you'll do in any domain, not just infosec or bb. So don't try to be Superman and avoid the signs that your body & brain might send. Listen to them and act on them. Relax. `Live to fight another day, and hit it Stronger & Harder`.

<a name="seventh-question"></a>
### :round_pushpin: Which domain you love most in security industry and why?

If you mean in an Offensive or Defensive sense, I'd say Offensive, hands down. It is much more of not just hacking at a technical level, but it's more of hacking at a Psychological level as well, trying to get into the head of the Developer and trying to understand his way of thinking while coding a particular app/function. And if you meant by the Niche in Offensive, maybe Web/APIs for now just because I'm more into it. But I guess Reversing is quite interesting as you actually have to mess around with Low-level System stuff quite down the OSI Model. So practically, it's just messing around at the Base/Core of everything.

<a name="eighth-question"></a>
### :round_pushpin: How to find new areas of research like James Kettle did?

Haha! This is quite far-fetched for me to answer. It's been just around 1.5 Years since I started into the Infosec field. And barely around 8-10 months of getting into bb. TBH, the more I learn, the more I understand that I barely know anything. But if there's something to be said, I'll say that **"Curiosity is the mother of Invention."** If you're curious enough, if you don't take anything as it is and keep asking the right questions, if you're ready to look beyond Money or Fame, and if you're determined & dedicated enough, I don't think there's anything the world that could stop you, an ordinary person from doing extraordinary things.

<a name="ninth-question"></a>
### :round_pushpin: Throw some light on Android Security!

Nowadays, Android is main OS of many devices like Smartphone, Smart Watch, Smart TVs and many more things based on Android. Most of the corporate domains and companies are shifting their whole businesses on Mobile Platforms. That's why we have more chances to get paid through Android Security. There are many resources available on internet to start from. As of now, I have less knowledge about Android! I've wanted to look into this for quite some time now but unfortunately haven't got around doing it. Hopefully soon :)

<a name="tenth-question"></a>
### :round_pushpin: At last, what you want to say something to fellow peeps?

It might seem like it at times, but Life isn't just a part of Infosec. Infosec is just a small part of your Life. In the pursuit of getting too digitally engaged, don't get disengaged from the actual Reality. The journey is what actually matters rather than the Result. Stop looking for shortcuts and stop stressing over too much. Keep going, Keep Growing. 1 step at a time. And don't forget actually to Live and enjoy Life :heart:

<center><b>I'm on <a href="https://www.buymeacoffee.com/iamsarvagyaa" target=_blank>buymeacoffee</a>, you can join with me on buymeacoffee :smile:</b></center>