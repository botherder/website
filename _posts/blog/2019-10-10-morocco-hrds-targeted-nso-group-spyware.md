---
layout: post
title: Moroccan Human Rights Defenders Targeted with NSO Group's Spyware
newsletter: True
categories: blog
---

At this point, this is almost not surprising. Pegasus, the spyware product from the infamous Israeli company NSO Group, has by now been found used against human rights defenders (including a colleague of mine at Amnesty), journalists and dissidents from UAE, Mexico, Saudi Arabia, and now Morocco, as we tell in our latest report:

English: [https://www.amnesty.org/en/latest/research/2019/10/Morocco-Human-Rights-Defenders-Targeted-with-NSO-Groups-Spyware](https://www.amnesty.org/en/latest/research/2019/10/Morocco-Human-Rights-Defenders-Targeted-with-NSO-Groups-Spyware)  
French: [https://www.amnesty.org/fr/latest/research/2019/10/Morocco-Human-Rights-Defenders-Targeted-with-NSO-Groups-Spyware](https://www.amnesty.org/fr/latest/research/2019/10/Morocco-Human-Rights-Defenders-Targeted-with-NSO-Groups-Spyware)  
Arabic: [https://www.amnesty.org/ar/latest/research/2019/10/Morocco-Human-Rights-Defenders-Targeted-with-NSO-Groups-Spyware](https://www.amnesty.org/ar/latest/research/2019/10/Morocco-Human-Rights-Defenders-Targeted-with-NSO-Groups-Spyware)  

It seems to me that NSO Group is racking up maybe even more documented cases of abuse of their products than other companies, such as FinFisher or HackingTeam, did in the past. Although companies' conduct and lack of due diligence contributes to this worrying trend, it is rather symptomatic of the ecosystem of industrialized government hacking which has been flowrishing in recent years.

In this latest report we detail how Maati Monjib and Abdessadak El
Bouchattaoui, respectively a prominent activist and academic and a well-known human rights lawyer, have been targeted using NSO Group's Pegasus spyware from 2017 onwards. In both cases we collected several malicious SMS messages carrying links to known NSO infrastructure.

## Social Engineering is a Craft

Similarly to previous cases, the messages attempt to lure victims through social engineering. At times the messages are political. For example, one message sent to Maati translates like following:

> *"Jerusalem will remain the capital of Palestine! Save the holy city by signing this petition: [exploit link]"*

More often, messages are designed to appear just like any other spam SMS victims might be used to receive. For example, the following text pretends to be a special offer from a large gym chain in Morocco:

> *"BlackFriday continues exceptionally today at CityClub! Last chance to get 15 months of fitness at 1633!  
> Tomorrow it will be too late  
> STOPSMS: [exploit link]"*

Interestingly, in multiple occasions the attackers sent the same text in repetition to purposefully simulate spam, irritate targets and, as shown above, offer the malicious link as an option to stop receiving such SMS messages. Nice trick.

Finding SMS messages such as this is a rare opportunity. Researchers seem to have so far only gathered evidence of such messages sent until about a year ago. It is possible NSO Group has since shifted tactics and realized SMS messages are too noisy and leave too many traces, and have instead invested in alternative attack vectors. Without knowing precisely what or how many 0day vulnerabilities can NSO rely on, determining a pattern of tactics is hard. For example, in 2019 NSO customers might have made large use of particular exploits (for example for WhatsApp or iMessage) as they became available. However, in 2020 the attack surface and the available capabilities might already look very different.

Through the course of this investigation, we found evidence that might indeed suggest NSO Group has some more cards up its sleeve.

## Network Injection Attacks

While analyzing Monjib's phone, we noticed a few suspicious web visits in his Safari browsing history that originated from clear-text initial connections to, for example, `http://yahoo.fr` and in less than 3ms redirected to URLs like this:

`hxxps://bun54l2b67.get1tn0w.free247downloads[.]com:30495/szev4hz`

(Note: the URL is edited with hxxps:// and [.] to avoid accidental clicks.)

In one occasion, few seconds after this visit, a suspicious process spawned and all the folders containing app crash logs appear to have been wiped. Crash logs (which you can view directly from the phone navigating to Settings > Privacy > Analytics > Analytics Data) contain details about application crashes, and in the case of exploitation would proove useful to identify the abused vulnerability. An attacker would definitely have an interest in making sure such logs wouldn't be available to security researchers or to Apple, in order to prevent the bug from being patched. These logs are normally stored indefinitely unless the iPhone is *synced* with iTunes, and we believe that the deletion from Monjib's phone right after what appears to be a malicious web redirect is evidence of what might be a **network injection attack**.

What exactly happened?

If our theory is correct, Monjib tried to visit `yahoo.fr` in order to access his mailbox from the phone, but his Internet connection was being monitored and automatically hijacked whenever he would visit an unencrypted web page (in this case `http://yahoo.fr`, but it could be any website without TLS) in order to inject a redirect and force Monjib's Safari to visit an exploitation server. If successful, the exploitation server would leverage a vulnerability in Safari and ultimately install the spyware.

The exploitation process would be the same as by sending malicious links via SMS, but through these automatic network redirects the attackers do not have to rely on successfully luring the victim into clicking on the links, but it happens programmatically.

Therefore, this attack vector is way more reliable and leaves virtually no  traces visible to the victims. Because of this, network injections are also very hard to identify, document and, especially, reproduce.

This form of attack is not new. FinFisher and HackingTeam, for example, also offered similar capabilities to their customers (with FinFly ISP<sup id="a1">[1](#f1)</sup> and Infection Proxy respectively<sup id="a2">[2](#f2)</sup>). A leaked brochure from NSO Group also details this capability in what they call a "Tactical Network Element"<sup id="a3">[3](#f3)</sup>.

## Conclusions

These cases of abuse are not isolated incidents, but they are establishing a, by now, very well documented pattern. Although less sophisticated attack platforms, such as phishing and commodity malware, represent a quantitavely larger threat to civil society, more sophisticated options such as Pegasus are a product of choice of more resourceful and determined attackers.

I worry it will become increasingly harder to detect and defend from these attacks. In this cat and mouse game, consumer technology vendors have to invest in hardening their products particularly in light of the reality that they are equally used by regular users as well as at-risk individuals. Ultimately, as these attacks become harder to develop, increasing their economic cost is critical to reduce instances of abuse. In the meantime, even UN officials are demanding a moratorium on the sale of surveillance technology in order to contrast these human rights violations<sup id="a4">[4](#f4)</sup>.

<span id="f1"></span>1: [https://wikileaks.org/spyfiles4/documents/FinFly-ISP-Catalog.pdf](https://wikileaks.org/spyfiles4/documents/FinFly-ISP-Catalog.pdf)  
<span id="f2"></span>2: [https://wikileaks.org/hackingteam/emails/fileid/595666/274112](https://wikileaks.org/hackingteam/emails/fileid/595666/274112)  
<span id="f3"></span>3: [https://www.documentcloud.org/documents/4599753-NSO-Pegasus.html](https://www.documentcloud.org/documents/4599753-NSO-Pegasus.html) 
<span id="f4"></span>4: [https://news.un.org/en/story/2019/06/1041231](https://news.un.org/en/story/2019/06/1041231)