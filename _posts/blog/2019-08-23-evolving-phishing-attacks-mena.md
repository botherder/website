---
layout: post
title: Evolving Phishing Attacks Targeting Human Rights Defenders in Middle-East and North Africa
newsletter: True
categories: blog
---
As you might have noticed, I've recently gone quiet on social media, as well as on this newsletter.  Life and its challenges took the most of me in the last few months. And while stepping away from social media was a great quality-of-life improvement I recommend to everyone, I apologize for the lack of regular content here.

Many of my previous newsletters have dealt with phishing. This is representative to the current state of digital threats faced by Human Rights Defenders (HRDs). As infecting devices becomes harder, we've been observing attackers develop and evolve their tactics at both the "low-tier" as well as the "higher-tier" of attack sophistication. At Amnesty International we track these campaigns of attacks and we are in the process of publishing reports about some of our most recent findings. In the lower tier, phishing remains dominant and as service providers implement mitigations, and security educators promote them, attackers work around them.

Last December we disclosed a campaign of large-scale targeted phishing attacks capable of systematically bypassing traditional forms of Two-Factor Authentication<sup id="a1">[1](#f1)</sup>. In March we disclosed a separate campaign of targeted phishing attacks using malicious third-party OAuth applications<sup id="a2">[2](#f2)</sup>. Two days ago we disclosed a renewed campaign, operated by the same attackers as the first, yet again with some evolved tactics:

[https://www.amnesty.org/en/latest/research/2019/08/evolving-phishing-attacks-targeting-journalists-and-human-rights-defenders-from-the-middle-east-and-north-africa/](https://www.amnesty.org/en/latest/research/2019/08/evolving-phishing-attacks-targeting-journalists-and-human-rights-defenders-from-the-middle-east-and-north-africa/)

OAuth Phishing<sup id="a3">[3](#f3)</sup> seems to be an increasingly popular tactic, most likely because of its simplicity as well as because, by nature, it enables attackers to avoid worrying about Two-Factor Authentication. Normally OAuth Phishing is conducted by creating malicious third-party apps that, once authorized to a victim account (for example, a Google or Outlook account), would siphon off all emails and other data. Consequently platform providers have started heavily cracking down on malicious third-party apps, and introducing stricter verification and authorization procedures for third-party apps developers.

Most likely in response to this, in this latest campaign the attackers have developed a new OAuth Phishing variant technique we had not observed before. Instead of creating malicious third-party apps, they found a way to abuse legitimate Google third-party apps in order to phish for victims accounts. Truthfully, we were quite impressed with the attackers' craft and ingenuity. I invite you to read the blog post for all the details (and pictures!).

## Some additional resources

Over the last year I have been working on a set of tools to facilitate the identification and reporting of phishing and spearphishing attacks. Currently it is in a closed-beta phase, but if you are a journalist, HRD or part of an NGO, and you are interested in hearing more, please do get in contact with me.

Lastly, over the last months I have produced a (still under development) Guide to Phishing that is published by Security Without Borders here:
https://guides.securitywithoutborders.org/guide-to-phishing/
It goes in to details on how phishing attacks work and what are the available mitigations. I hope you will find it useful. Any contributions are welcome!

<span id="f1"></span>1: [When Best Practice Isn’t Good Enough: Large Campaigns of Phishing Attacks in Middle East and North Africa Target Privacy-Conscious Users](https://www.amnesty.org/en/latest/research/2018/12/when-best-practice-is-not-good-enough/)  
<span id="f2"></span>2: [Phishing attacks using third-party applications against Egyptian civil society organizations](https://www.amnesty.org/en/latest/research/2019/03/phishing-attacks-using-third-party-applications-against-egyptian-civil-society-organizations/)  
<span id="f3"></span>3: [Guide to Phishing - Security Without Borders](https://guides.securitywithoutborders.org/guide-to-phishing/oauth-phishing.html)
