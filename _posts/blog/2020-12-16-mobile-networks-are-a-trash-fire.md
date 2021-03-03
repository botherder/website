---
layout: post
title: Mobile Networks Are A Trash Fire - Exhibit Nr. 16384
newsletter: True
categories: blog
---

The Bureau of Investigative Journalism just published, jointly with The Guardian, [the findings of an investigation into the murky relationship between the surveillance industry and mobile operators](https://www.thebureauinvestigates.com/stories/2020-12-16/spy-companies-using-channel-islands-to-track-phones-around-the-world). In particular, they revealed how the Channel Islands have become a nexus of malicious SS7 traffic directed all over the world through access provided by two operators in particular, Sure Guernsey and Jersey Airtel. TBIJ found Rayzone Group, an Israeli surveillance vendor, as a key supplier of SS7-based monitoring solutions.

SS7, or Signaling System No. 7, is a set of protocols from the 1980-1990s used to instantiate calls, handle billing, and a number of other operations carried out by telecommunication networks operators, particularly when they need to talk to each other because their subscribers are, for example, connected from abroad. While in theory access to SS7 should be reserved to accredited operators only, in practice it's a wild west. Why? Because surveillance vendors, intelligence agencies, and malicious actors of all sorts, make great use of the capabilities SS7 can provide, including tracking the geographical location of a phone number, and intecepting calls and SMS messages.

In 2014 already, Tobias Engel gave a compelling presentation on the [vulnerabilities of SS7 at 31c3](https://www.youtube.com/watch?v=-wu_pO5Z7Pk). In it, Tobias stated *"getting access is easier than ever: can be bought from telcos or roaming hubs for a few hundred euros a month; usually (not always), roaming agreements with other networks are needed, but some telcos are reselling their roaming agreements; some network operators leave their equipment unsecured on the internet."* In 2015 folks from Berlin-based SRLabs made a splashing appearance on [Australian 60 Minutes](https://www.youtube.com/watch?v=1oA0O01SQUE), demonstrating many of the same issues. In 2017 journalists reported on [a spree of bank accounts takeovers](https://www.wired.com/2017/05/fix-ss7-two-factor-authentication-bank-accounts/) conducted by criminals who obtained access to SS7. So, while risks associated with SS7 have been widely known for many years, this most recent investigation by TBIJ caught red-handed companies enabling these abuses for the first time.

Other than [Rayzone Group](https://rayzone.com/solutions/) and NSO Group/[Circles](https://citizenlab.ca/2020/12/running-in-circles-uncovering-the-clients-of-cyberespionage-firm-circles/), a quick Google search will reveal [numerous](https://www.intercept.ws/catalog/3227.html#desc1) boutique [shops](http://www.itmaxglobal.com/telecom-security/) of varying degrees of sketchiness offering tracking and interception of mobile phones. Some only offer software and hardware products, implying customers already have access to SS7, others instead sell it as a service. Ironically, publicly available brochures even suggest some of the more established surveillance vendors might even be members of organizations such as 3GPP, which develop standardized protocols for telecommunications.

Human rights defenders inevitably face heightened risks. **Throughout 2020 we've observed a growing trend of attacks leveraging the ability to intercept SMS messages in order to take over social media and instant messaging accounts.** For example, Amnesty Indonesia [documented](https://www.amnesty.id/end-wave-of-digital-attacks-on-students-journalists-activists/) numerous cases of WhatsApp, Instagram, and Twitter accounts of activists being infiltrated seemingly through the attackers' ability to intercept SMS recovery and two-factor authentication codes. Similar [news reports recently came out of Bangladesh](https://netra.news/2020/we-hack-facebook-state-sponsored-cybercrime-in-bangladesh-1137) as well. Evidence of these takeovers is piling up from everywhere.

While in some cases SS7 likely played a role, in others state-sponsored actors more likely favor these attacks because of direct leverage they might have on national mobile operators. In some countries state-owned operators monopolize the local market.

These attacks are trivial yet extremely effective. Because many online services rely on phone numbers as ultimate identification channels, an adversary capable of intercepting SMS messages could easily infriltrate accounts of targeted users. For example, one can request a password reset of a Facebook account, or connect a device to an existing WhatsApp account, and simply wait to intercept the verification codes sent via SMS to the victim. At the point the victim grows suspicious of the unsolicited message from Facebook or WhatsApp, it's likely too late. Besides snooping on private conversations wherever possible, we see attackers impersonating victims, spreading misinformation, or collect private pictures to publicly disseminate for reputational damage.

The security community has been [viciously debating](https://blog.cmpxchg8b.com/2020/07/you-dont-need-sms-2fa.html) about the effectiveness of SMS-based two-factor authentication, although primarily in relation to phishing attacks which would require the targets to volunteer their verification codes to look-alike login pages. However, for those whose adversaries are capable of intercepting messages the attack scenarios I described are much more pernicious and harder to protect against. In my perhaps unpopular opinion, despite being better than none in most use cases, SMS verification has only become a liability for activists, journalists and other vulnerable communities. In those cases, it might even simplify the attackers' lives.

While we need to continue equipping as many at-risk users as possible with hardware security keys, the tech sector needs to re-think current verification procedures and democratize access to more secure authentication protocols. Above all, a more dedicated debate around the oversight and accountability of mobile network operators is long overdue. They are no longer *"just"* carriers of our phone conversations, but have become gatekeepers of our digital identities too. Consumers are required to place enormous trust in these companies, some of which regularly betray it with impunity. We need to urge companies to not concede to the surveillance industry and to adopt all available mitigation strategies.