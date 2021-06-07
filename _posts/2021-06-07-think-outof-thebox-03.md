---
title: "Think outside the box with Devansh Batham"
author : Sarvagya Sagar
excerpt_separator: "<!--more-->"
image:
    path: /images/ama-session/03.png
    thumbnail: /images/ama-session/03.png
categories:
    - Interview
tags:
    - Bug Bounty 
    - Unicode Normalization
    - AMA Session
---

Hey, everyone. I hope you all are safe in this pandemic. After a long time, I am back with an interview session. So, today's guest is Devansh Batham, aka Asm0d3us. He is currently working as a triager at HackerOne, and also he created a lot of tools. He gave wonderful answers to all the questions, I am delighted with his answers. Thank You, so much Devansh! :heart: for all the well-explained answers and also for creating awesome tools. Please check out his open-source tools and his blog posts. This is the third post in series of Interviews. Let’s get started!

<!--more-->

-   [How did you started and What got you into hacking?](#first-question)
-   [Your methodology and workflow to hunt bugs?](#second-question)
-   [Your approach to learning new things?](#third-question)
-   [How do I stay motivated after getting duplicates and N/A?](#fourth-question)
-   [What advice do you want to give to all of us?](#fifth-question)
-   [How you manage your mental health, and burnout?](#sixth-question)
-   [How to find new areas of research like James Kettle did?](#seventh-question)
-   [Throw some light on Unicode Normalization!](#eighth-question)
-   [Which bug you love most and why?](#ninth-question)
-   [At last, what you want to say something to fellow peeps?](#tenth-question)

![Devansh Batham]({{ '/images/ama-session/interview-03/devansh.png' }}){: .align-center}

- Twitter Handler - [https://twitter.com/0xAsm0d3us](https://twitter.com/0xAsm0d3us)
- Github Profile - [https://github.com/devanshbatham](https://github.com/devanshbatham)
- LinkedIn - [https://www.linkedin.com/in/devansh-batham](https://www.linkedin.com/in/devansh-batham)
- Medium - [https://medium.com/@Asm0d3us](https://medium.com/@Asm0d3us)

<a name="first-question"></a>
### :round_pushpin: How did you started and What got you into hacking?

I first heard about **"Hacking"** when I was in 8th standard; at that time, I got hooked by this concept, however, I had no idea how it works? I thought of it as some magical stuff. I got my first PC in 9th standard, and probably around that time, my learning curve started; by this time, I had a basic understanding of HTML/JS/XML, the first bug class that I learned about was `error-based SQL injection`, as back in the time most of the web apps were written in PHP with SQL DBs for data storage, therefore those applications were very much prone to SQL Injection vulnerabilities.

Soon I started participating in *BBPs and VDPs*, in the initial days, most of my findings were `XSS, Misconfigured OAuth implementations, SQL Injections`, etc. (basically most of OWASP Top 10). The initial days were good, I was scoring good bounties, and everything was going well and fine; however, I was a little dissatisfied as my learning curve was not moving at the desired pace. Therefore I took a break for 6 months and got myself into learning GoLang, now with good scripting skills, it was much easier for me to automate my hunting, and it produced some excellent results.

In 2018, I took admission to college, and I was devoting most of my time there to learning new attack vectors and sharpening my automation skills. After gaining about 5-6 years of experience in this Bug Bounty industry, I joined **HackerOne** full-time as Security Analyst.

<a name="second-question"></a>
### :round_pushpin: Your methodology and workflow to hunt bugs?

The answer depends on what you understand by a **"methodology"**? Running a lot of DNS enumeration tools one after another until you find a subdomain that resolves to an IP address is a methodology? Scanning for open ports, then fingerprinting them, and passing the output to some other **"fancy"** tool is a methodology? Crawling and scraping JS files until you find some hidden creds or tokens is a methodology? That is the problem; people focus so much upon building methodologies and **"copying"** what others do, they forget what they really should be doing. I try to keep things as simple as possible, Methodology is more like a mindset, and no two people can have the same mindset, what works for others might not work for you, and it takes time to find what works for you, there are no shortcuts and believe me most of those **"cheap"** courses that claim to teach you bug-bounty methodologies are just not worth it. :raised_hand_with_fingers_splayed:

{: .notice--success}
I believe we should not stick to any particular methodology, you should keep experimenting with different approaches and techniques, and you will eventually find what works best for you.

<a name="third-question"></a>
### :round_pushpin: Your approach to learning new things?

The best way to keep your learning curve step is by doing and learning things that are out of your comfort zone, and one should move on from their comfort zone as soon as possible, this industry is changing rapidly, and we really cannot get comfortable and stick with any particular skill or niche, and this applies to almost every industry. I will cite a paragraph as an example from the `Kodak failure case study` that shows why it is very crucial not to get comfortable with any one particular thing:

"**Kodak** was the most dominant company in its field for almost the entire 20th century. But a series of wrong decisions killed its success. As technology progressed, the use of films and printing sheets gradually came to a halt. This was due to the invention of digital cameras in 1975. However, Kodak dismissed the capabilities of the digital camera and refused to do something about it. Did you know that the inventor of the digital camera, *Steve Sasson*, was an electrical engineer at Kodak when he developed the technology? When Steve told the bosses at Kodak about his invention, their response was, **“That’s cute, but don’t tell anyone about it.”** That's how you shoot yourself in the foot! " The full case study can be found here: [https://startuptalky.com/kodak-bankruptcy-case-study/](https://startuptalky.com/kodak-bankruptcy-case-study/).

Now try to understand this in the context of the cybersecurity industry, with AI and ML, a lot of testing can now be automated, newly-developed frameworks have pre-built `CSRF/XSS/SQL Injections` defenses (and they work fine in "most" of the cases), so stay informed about latest trends and keep up with what is happening around you in this industry, that's how I prefer to learn new things, i.e., by not getting very comfortable with any one particular niche.

<a name="fourth-question"></a>
### :round_pushpin: How do I stay motivated after getting duplicates and N/A?

My Duplicate/Na % is very low, and here is a "secret" tip on how you can achieve that too: Before submitting any bug, ask yourself, *"How can an attacker leverage this behavior into crafting a real-world or practical exploitation scenario?"* and if you can't figure out a possible scenario, then don't submit. Submitting `"Password reset link not expiring"` and not expecting to be a duplicate is like standing in rain expecting not to get wet.

<a name="fifth-question"></a>
### :round_pushpin: What advice do you want to give to all of us?

I will be precise on this, and try to give my answer in points:
- Learn things that are out of your comfort zone.
- Take proper notes of whatever you are learning.
- Try to practice kindness and patience; always practice respect.
- There is always someone smarter than you, and you need to accept that fact.
- Look back on past mistakes as learning experiences, not as regrets

<a name="sixth-question"></a>
### :round_pushpin: How you manage your mental health, and burnout?

The real question is, how do we know when we’re suffering from it? I look for three potential symptoms, `"Exhaustion," "Alienation," and "Reduced performance,"` and if I feel like I am going through any one of them, I try to take small breaks, and that works well for me.

<a name="seventh-question"></a>
### :round_pushpin: How to find new areas of research like James Kettle did?

Try to choose a research area that is outside of your comfort zone, by doing this, you will expand your boundaries and learn a ton of new things. If you want inspiration, you can browse through a lot of research papers from here: [https://paper.seebug.org](https://paper.seebug.org/) ...

<a name="eighth-question"></a>
### :round_pushpin: Throw some light on Unicode Normalization!

Here is a formal definition, *"Unicode Normalization Forms are formally defined normalizations of Unicode strings which make it possible to determine whether any two Unicode strings are equivalent to each other. Depending on the particular Unicode Normalization Form, that equivalence can either be a canonical equivalence or a compatibility equivalence."* The use-cases are immense, few examples are XSS filter bypass, WAF Bypass, SSRF defense bypass, etc.

It is not possible for me to explain it in one paragraph `(I have an article in my drafts that explains the art of filter/WAF bypass using Unicode in detail, that will be very releasing soon)`, the meantime if you want to understand it in-depth, then you can refer to the standard Annexure from here: [https://unicode.org/reports/tr15/](https://unicode.org/reports/tr15/) ...

<a name="ninth-question"></a>
### :round_pushpin: Which bug you love most and why?

XXE! They are often overlooked, and the impact is always either High or Critical, they allow an adversary to view files on the application server file system, in some cases, they can be leveraged into RCE as well. Here is an awesome resource to learn about XXE - [https://gosecure.github.io/xxe-workshop/](https://gosecure.github.io/xxe-workshop/)

<a name="tenth-question"></a>
### :round_pushpin: At last, what you want to say something to fellow peeps?

- Learn something new every day.
- Trust your instincts.
- Do what is right, not what is easy
- Treat others the way you want to be treated
- Build **"soft-skills"**, they are very essential.

<center><b>I'm on <a href="https://www.buymeacoffee.com/iamsarvagyaa" target=_blank>buymeacoffee</a>, you can join with me on buymeacoffee :smile:</b></center>
