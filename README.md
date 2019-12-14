# Nathaniel Rogers - Assignment 1

<style type="text/css">
a {
    color: #b5e853;
    text-shadow: 0 0 5px #b5e853
}
</style>

Welcome to my RMIT-intro2IT-A1 intro page!

[Navigator](#)
- [About Nathaniel](#about-nathaniel)
- [Job Listing](#job-listing)
- [Personality](#what-is-my-personality-like)
- [Project Idea](#my-awesome-untitled-project)

### About Nathaniel
![It's my face](.img/me.png)
A little about me to start. I'm Nathaniel, student ID s3829502, (email: [s3829502@student.rmit.edu.au](mailto:s3829502@student.rmit.edu.au)) 25 living in Queensland, away from home and the dream to be a big grown up living in my own house was a brilliant scam, because life is so much harder as an adult. Apparently there is such thing as too much cake! (I digress) I was born and raised in Australia, moving between Queensland and New South Wales until I took two years to volunteer as a missionary for my church in Scotland and Ireland which now holds a dear place in my heart.

My Dad worked for an internationally known IT company my whole childhood so I cant really remember a time when we weren't using technology, but because it was what my dad did I didn't think it would be cool to also go into that field so I tried art instead in high school. Long story short, I was failing art so I changed to IT and everything just made sense so I succumbed and realised my future would be in IT.

![Pinball Windows 95 (image from http://www.neoegm.com/wp-content/uploads/2009/08/Pinball_Cracker_Game.png)](./img/pinball.png)

*I remember spending way too much time playing this pinball game because someone was using the phone so we couldn't ALSO be on the internet. Good ol' dial up.*

I have been working for an e-commerce agency (www.neocreative.com) for three years doing module development primarily in PHP.
[<img src="./img/neocreative-logo.png">](http://www.neocreative.com/)

### Job Listing
So, being a hacker is very glamorous in movies, but doing illegal things with the risk isn't really something I want to do. Kinda conflicts with my morals. That is where penetration testing comes in.
A penetration tester is someone who is referred to as a "white hat" hacker because their job is to test companies cyber security, at their request (this is the key difference), to determine any potential threats/exploits and help the companies to secure against them, before a malicious "black hat" hacker finds them and exploits them.

There are plenty of job listings out there for penetration testing, but here is an example.
[https://www.seek.com.au/job/40557657](https://www.seek.com.au/job/40557657)

![Job Listing Screenshot](./img/pentesting_job_ad_description.png)

This position is appealing to me because it would require me to already have some experience with penetration testing (pentesting). Being able to have mentoring while working would beneficial to improve my skills.
The skills that would be required are:
- A strong networking understanding
- Being up to date with common attack vectors and vulnerabilities
- Ability to write a professional report
- Understand what "red team engagements" means
- A good understanding of windows and linux based command line interfaces/programs

The skills I currently have:
- A very basic understanding of networking
- The ability to write reports
- A good understanding of Powershell and Teminal usage and basic (batch, ps1 and bash) script writing

In order to increase my networking skills I have been trying to do CTF challenges (which are sandboxed pen testing challenges available to anyone)
I will need to familiarise myself with the terms used in the industry, which I imagine would come with talking with someone in the industy, looking at example reports, studying specific cyber security classes and just getting experience in the industry.

### What is my personality like?
In the [Myers Briggs personality test](https://16personalities.com) the result I got was "[The Mediator](https://www.16personalities.com/infp-personality)" (INFP)

The learning style result I got was that I am a visual learner
![Visual Learner (https://www.how-to-study.com/learning-style-assessment/)](./img/learning_style_results.png)

I chose to take the Big Five Personalities Test to learn more. Turns out my highest quality is in Openness
![Big Five Results (https://www.truity.com/test/type-finder-personality-test-new)](./img/big_five_results.png)

These results mean that you can count on me to try and keep the peace between group members. That's generally at my own expense, but at least we will get the project completed. I'm a big fan of people having separate (not necessarily equal) responsibilities that each member feels is within their ability, so divying up the group work is probably where I will be able to be most useful.

### My Awesome Untitled Project

*just brainstorming names:*
- Quarentyne
- ClosedOff
- SafeBrowse

#### Overview
The project that I have come up with is to implement containerised based web page viewing restircting any access to the computer's actual files. The idea would be some sort of sandbox environment that employees can use to view emails, websites etc that are potentially malicious without the risk of the companies confidential data being tainted or exposed. This could be expanded to a physical device much like a USB stick that automatically runs the safe container as a layer between the web client and the server.

#### Motivation
There has been an uprise in Malware attacks. According to Statistica, there were 10.52 billion malware attacks in 2018. Focusing on ransomeware, which is when a malicious player somehow crypto-locks all the files on the computer and demands a ransom to have the files decrypted, companies have been forced to pay a large ransoms with the hope that they get their files back, or simply lose their archives. This is a big issue that has been known to be triggered by phishing attacks, Man in the Middle attacks or even just a malicious google result. The first point of call is to limit access for the employees so in a worst case scenario only that single employees files will be locked. However this causes issues with development requirements or other business requirements.
<a href="https://www.statista.com/statistics/873097/malware-attacks-per-year-worldwide/" rel="nofollow"><img src="https://www.statista.com/graphic/1/873097/malware-attacks-per-year-worldwide.jpg" alt="Statistic: Annual number of malware attacks worldwide from 2014 to 2018 (in billions) | Statista" style="width: 100%; height: auto !important; max-width:1000px;-ms-interpolation-mode: bicubic;"/></a><br />Find more statistics at  <a href="https://www.statista.com" rel="nofollow">Statista</a>

#### Description
The idea for this project is to use containerisation technologies (see [Docker](https://www.docker.com/) for example) to isolate the web browsing experience and avoid getting infected by malware. This tool would need to be used by people with little to no information security knowledge as experienced people in the industry would be able to identify or stop the attacks (generally) before their computers become infected. This could be installed as a sort of safe proxy type network for use in schools, hospitals, enterprise companies or individually for personal computing. When a TCP packet comes through to the network, this container would act as a reverse proxy server and return the HTTP request in the container, which could then have some sort of intelligent malicious code detection built in to determine whether the file system is trying to be modified, or accessed suspiciously, etc. This could then flag the site as malicious and have a big warning added to the email or google result or whatever medium the web user is trying to access the site, warning them to proceed with caution. Alternatively it could just remove the access to that site altogether. This would be handy for increasing awareness of cyber attacks in the workplace and decreasing their effectiveness. A systems administrator would then be emailed a report of all the malicious sites that have been detected and work on protecting against those attacks and try to get the malicious sites taken down/block ip addresses or email addresses etc. As this is relying on containerisation, if there are any exploits that can change access from the guest container to the host machine, a malicious actor could potentially by pass this safety measure all together.

#### Tools and Technologies
The software that will be used for this project would be some sort of containerisation software. Docker with a combination of orchestration software such as docker compose or Kubernetes is well known in the dev-ops industry for the future of web hosting, so using that would probably be easiest. The technical requirements are simply that the processes on the machine won't have access to any actual file system or user that has access to confidential data, which could include writing a back door, logging the keystorkes, etc. All of those vectors would need to be inaccessible to the container. The USB type device would need to interface with all the different operating systems at a low level and intercept all TCP packets to first run them in the quarentined environment.

#### Skills Required
The containerisation software is free and readily available. Writing the malicious code detection software would probably be the trickiest part of this project as there are so many ways to modify the output so that it doesn't look suspicious (encoding, minification, obfuscation). Looking at the resultant file set, and comparing it with the file set before the site was browsed, would be a way to determine malicious activity (or at the very least, suspicious as the file system changed). You would need to exclude paths that are expected to change, such as the cached directories and the user settings paths. Writing this into the network layer as a reverse proxy would require a sound knowledge of servers like apache and nginx, as this would be doing a very similar thing. 

#### Outcome
If this project is successful at intercepting network traffic and running sites in an isolated environment it would significantly limit how much data is leaked within companies and how many systems are compromised. I am unaware of other products which do this sort of process isolation and believe this will be a good product for anyone wanting to combat cyber security breaches in the future. Limiting the cyber security attacks effectiveness will overall mean there will be less attacks, or will force the black hat hackers to come up with ways to gain access to the host machine from within the container. In IT there is no such thing as impenetrable security, but ideally this would make breaches easier to detect and therefore protect against.
