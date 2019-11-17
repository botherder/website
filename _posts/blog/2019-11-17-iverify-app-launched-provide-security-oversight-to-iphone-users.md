---
layout: post
title: iVerify App Launched To Provide Security Oversight and Recommendations to iPhone Users
newsletter: True
categories: blog
---

2019 was a brutal year for mobile security already<sup id="a1">[1](#f1)</sup>, and hopefully no more surprises linger around the corner in the remaining weeks of this year. I recognize now this topic dominated even this same newsletter and, in the best tradition of my ranty content, it featured mostly my own frustrations.

This week US security firm Trail of Bits released iVerify<sup id="a2">[2](#f2)</sup>, a tool to verify the integrity of an iPhone and harden it by guiding users through various configuration steps.

The app costs about 6 euros, and if you can afford it you might find worth trying it out. I am enjoying it. Regardless, its release provides me with a good opportunity to discuss some of its functionality and security recommendations for iPhone users, and explain their rationale.

iVerify leverages Trail of Bits' commercial "iverify-core" library normally sold to app developers interested to check whether the phone is jailbroken or not. Banking apps, for example, often leverage such frameworks in order to prevent execution on potentially compromised devices. While the fine folks at Trail of Bits are widely respected experts in the field of cyber security, I can not attest to the comprehensiveness of its detection engine without some longer experimentation on the field. It is quite possible iVerify won't catch the likes of NSO Group in all circumstances, but any clue of a potential compromise helps. Therefore, while you should not blindly trust a green tick labelling your phone as "Secure", **any warning message might be a good reason to worry**.

What I found more interesting to discuss instead are the configuration options iVerify suggests in a collection of short step-by-step guides. There are many of them, some about privacy or device theft, and some about iOS security. I am going to concentrate on the latter.

Limit Software Exploits
-----------------------

The recommendations in this category are aimed at offering the best available configuration for your iPhone to reduce as much as possible the attack surface.

### 1. Enable Automatic Updates
This might seem the most obvious, falling behind on iOS releases can happen. Staying up-to-date with latest software updates turns you immediately into a slighlty harder target to attack. **Make sure to have Automatic Updates enabled.**

### 2. Disable AirDrop / Bluetooth / Personal Hotspot
With the aim to reduce my own attack surface, I tend to never use services such as AirDrop. Trail of Bits suggests to disable AirDrop too, particularly in light of past vulnerabilities<sup id="a3">[3](#f3)</sup>. Similarly, Bluetooth and Personal Hotspot are proximity network services that might offer potential entry points for attackers in the vicinities, if the exposed network stacks contain vulnerabilities.

### 3. Disable JavaScript in Safari
Attacks that leverage exploits in the browser have reduced significantly on desktops in recent years, but appear again and again in targeted attacks on mobile<sup id="a4">[4](#f4)</sup>. They most commonly manifest through malicious links sent via SMS or instant messengers or, as my team at Amnesty documented in a recent report, through network injection attacks hijacking insecure website visits<sup id="a5">[5](#f5)</sup>. In order to instrument and deliver the exploit, JavaScript is almost always involved. Interestingly, Safari allows to disable JavaScript entirely, which should drastically disable browser exploits from functioning correctly.

I have been experimenting for a while with this configuration myself, and I can confirm it breaks most of the websites I end up visiting. You could decide to disable JavaScript in Safari and use it to visit unsolicited or suspicious links, and have a dedicated separate browser (such as Chrome or Firefox) for your own browsing. However, this requires some diligence on your part, and it sacrifices some additional mitigations we'll discuss later. If the security of your smartphone concerns you particularly, perhaps you might want to consider accepting some sloppy JavaScript-free browsing.

### 4. Upgrade to A12 CPU or higher
As iVerify rightfully points out, newer iPhone generations come with some important exploit mitigations. Above all Pointer Authentication Codes (PAC), which is only available from the iPhone X series. In the previous newsletter I already addressed<sup id="a6">[6](#f6)</sup> my concerns around the problematic unavailability of decently secure mobile devices in the lower/mid price range. Mitigations such as PAC, and the more to come in the future, can make a significant difference, but if you want to take advantage of this improvement you would need the financial resources to make a pricey upgrade.

### 5. Periodically reboot your device
Security measures in iOS increase the difficulty for attackers to maintain persistence over a compromised iPhone, even after a successful exploitation. Rumors I heard, and recent reports<sup id="a7">[7](#f7)</sup>, suggest that some threat groups are turning to opportunistic smash-and-grab attacks precisely to avoid dealing with obtaining a permanent installation of their malware. Periodically rebooting your device can help cleaning up leftovers and perhaps disabling an existing infection that is not able to survive it.


Review for signs of compromise
------------------------------

Recommendations in this section are rather basic, but unfortunately as much that is possible to a user. I discussed the difficulty of inspecting mobile devices for signs of a compromise in a previous newsletter.

### 8. Remove unknown devices from iCloud
You might have some older devices you no longer use connected to your iCloud account, or you might find devices you do not recognize at all. If your iCloud account was compromised, perhaps through phishing, attackers might connect a separate device to it in order to synchronize data and files you create. Removing<sup id="a8">[8](#f8)</sup> your own unused devices from your account is also a good practice to exercise.

### 9. Look for suspicious Apple Profiles
In order to manage fleet of phones, enterprises often deploy Mobile Device Management (MDM) platforms. Through MDM, administrators are able to, among other things, monitor the location of the enrolled phones, enforce specific configurations, or install apps. Some threat groups have been found using social engineering to enroll targeted phones with malicious MDM servers under their control and use them, for example, to deploy malicious apps<sup id="a9">[9](#f9)</sup>. If an iPhone is enrolled with an MDM server, a profile should appear in the Settings. Checking those profiles, as suggested by iVerify, might reveal some you don't recognize which you are able to remove.


Network security
----------------

The Network Security section only provides one recommendation to enable a particularly interesting feature iVerify has.

### 10. Safari Content Blocker
Safari allows developers to create Content Blocker extensions. Apps such as AdGuard leverages this to block advertisement networks and other unwanted web resources. iVerify uses this too, but to automatically redirect unencrypted HTTP visits to HTTPS, if supported by the website. If it doesn't, iVerify's Content Block will stop the insecure request and display a warning. You can test this by visiting www.neverssl.com with Safari.

While the general intent is to prevent accidental data leakage, especially over insecure networks (such as open Wi-Fis), this feature will also help mitigating network injection attacks such as those described in Amnesty's "Morocco: Human Rights Defenders Targeted with NSO Group's Spyware"<sup id="a5">[5](#f5)</sup> report. Network injection allows attackers to programmatically hijack insecure HTTP connections to any website and redirect the target to an exploitation server which will attempt to compromise the iPhone through, for example, vulnerabilities in the Safari browser.

By blocking visits to HTTP sites, iVerify *should* (I'm using caution here, because I have not actually tested this yet) help you prevent these attacks, so long as you use Safari for all your web browsing. Content Blockers have no effect over other browsers you might have installed, such as Firefox or Chrome.



<span id="f1"></span>1: [https://www.vice.com/en_us/article/bjwne5/malicious-websites-hacked-iphones-for-years](https://www.vice.com/en_us/article/bjwne5/malicious-websites-hacked-iphones-for-years)  
<span id="f2"></span>2: [https://blog.trailofbits.com/2019/11/14/introducing-iverify-the-security-toolkit-for-iphone-users/](https://blog.trailofbits.com/2019/11/14/introducing-iverify-the-security-toolkit-for-iphone-users/)  
<span id="f3"></span>3: [https://www.zdnet.com/article/apple-airdrop-flaw-leaves-users-vulnerable-to-exploit/](https://www.zdnet.com/article/apple-airdrop-flaw-leaves-users-vulnerable-to-exploit/)  
<span id="f4"></span>4: [https://arstechnica.com/information-technology/2019/09/webkit-zeroday-exploit-besieges-mac-and-ios-users-with-malvertising-redirects/](https://arstechnica.com/information-technology/2019/09/webkit-zeroday-exploit-besieges-mac-and-ios-users-with-malvertising-redirects/)  
<span id="f5"></span>5: [https://www.amnesty.org/en/latest/research/2019/10/Morocco-Human-Rights-Defenders-Targeted-with-NSO-Groups-Spyware/](https://www.amnesty.org/en/latest/research/2019/10/Morocco-Human-Rights-Defenders-Targeted-with-NSO-Groups-Spyware/)  
<span id="f6"></span>6: [https://nex.sx/blog/2019/11/11/the-economic-inequality-of-mobile-security.html](https://nex.sx/blog/2019/11/11/the-economic-inequality-of-mobile-security.html)  
<span id="f7"></span>7: [https://blog.malwarebytes.com/mac/2019/08/unprecedented-new-iphone-malware-discovered/](https://blog.malwarebytes.com/mac/2019/08/unprecedented-new-iphone-malware-discovered/)  
<span id="f8"></span>8: [https://support.apple.com/en-us/HT205064](https://support.apple.com/en-us/HT205064)  
<span id="f9"></span>9: [https://blog.talosintelligence.com/2018/09/ios-mdm-hide-the-app.html](https://blog.talosintelligence.com/2018/09/ios-mdm-hide-the-app.html)
