---
layout: post
title: The New Old Frontier of Interception
newsletter: True
categories: blog
---

States spend the big bucks on latest surveillance technology to have it easy. Emails and SMS messages carrying malicious attachments or links, for how crafty they might be, are not cutting it. Social engineering is unreliable, at times ineffective, and - damn it - its traces allow those pesky researchers to [keep catching attacks](https://securitywithoutborders.org/resources/targeted-surveillance-reports.html)!. As a matter of fact, I have lost count of the number of reports on NSO published thanks to malicious SMS messages trivially recovered from devices of journalists and activists. Certainly NSO's customers took notice and getting busted did not stop them, but rather made them pull out more cash from their deep wallets. And surveillance vendors go ca-ching!

Sometimes, I can't help but think that our exposures have likely helped these companies' sales teams convince customers to spend more and upgrade their attack tools to stealthier and more insidious spyware delivery vectors. And while a [0day vulnerability in WhatsApp](https://techcrunch.com/2019/10/29/whatsapp-spyware-nso-group/) might be a rare opportunity, other techniques can be more commonly available.

On June 22nd [we published a report](https://www.amnesty.org/en/latest/research/2020/06/moroccan-journalist-targeted-with-network-injection-attacks-using-nso-groups-tools/) on attacks against Omar Radi, a Moroccan journalist and human rights defender, using network injection attacks over his 4G mobile network. Those of you who follow this newsletter already know all about it. With a perfect timing, shortly thereafter [Netzpolitik revealed](https://netzpolitik.org/2020/staatstrojaner-provider-sollen-internetverkehr-umleiten-damit-geheimdienste-hacken-koennen/) the German secret service is attempting to pass a law to compel German mobile, Internet and service providers to facilitate similar network injection attacks in order to deliver spyware to targets in the country.

The principle is essentially the same: it's much better to automatically force a device to open a bad link unbeknownst to its owner, than trick the owner into opening it manually. How? You wiretap the network of the target, and at the first opportunity of an unencrypted request to either a website or a binary download, you hijack the connection and respond with malicious content instead of the original. This technique has been widely known to the hacking community for many years, and was "professionalized" in the surveillance industry in the early 2010s, for example by the [German FinFisher with FinFly ISP, and the Italian Hacking Team with their Infection Proxy](https://citizenlab.ca/2014/08/cat-video-and-the-death-of-clear-text/).

In those years attacks primarily targeted computers, rather than phones, although some sweet leaked documents from 2010 already detail, for example, [a country-wide deployment on mobile operators in Turkmenistan](https://sii.transparencytoolkit.org/docs/Dreamlab-Technologies_iProxy_Quotation_1sii_documents). Infecting computers through network injection only required the targets to receive an unencrypted iTunes update, or watch a YouTube video, or download anything from the Internet. Abracadabra, and without doing anything wrong, their devices would be infected.

HTTPS, which prevents - or at least complicates - network injection by encrypting the communication in transit, wasn't really as widely popular then as it is today. As a matter of fact, YouTube accelerated its full deployment of HTTPS only after being confronted with FinFisher and Hacking Team's network injection capabilities. Then, it really took Edward Snowden's revelations to significantly push HTTPS' adoption forward.

All that is to say network injection isn't new at all, but we are clearly seeing a resurgence in its popularity. Is it the new old frontier of interception?

These attacks are much more insidious to prevent and especially discover. Typically, in our work, people contact us because of emails or messages they received and they suspect to be malicious. If done properly, network injections leave very little traces for a target to be suspicious of, and consequently it reduces our ability to discover abuses.

Besides this, network injections also raise numerous concerns from privacy and consumer rights perspectives. For example, Netzpolitik reports, German authorities under this latest law proposal could compel not only Internet Service Providers, but also mobile operators, German Internet exchanges and even hosting companies such as Hetzner, to become auxiliary to these attacks. The inherent trust relationship that exists between these companies and their customers could be seriously undermined. Of course authorities always had the ability to leverage these providers' ability to monitor customers' communications, but facilitating the compromise of their personal devices represents an escalation.

However, if authorities want to target mobile devices, the cooperation of network providers isn't even necessary. The security trashfire that are mobile networks in fact allows attackers to use tactical network equipment, more commonly referred to as "IMSI catchers". If attackers are able to get in physical proximity of the target smartphone, they can deploy a rather portable device that will mimick a cellular tower, force the phone to connect to it, and combine access to SS7 (or the more modern Diameter network) to obtain decryption keys in order to inspect Internet traffic over 3G/4G, hijack web requests and redirect the victims to exploitation sites.

To find examples of such devices for sale, look no further than [some random](https://www.discoverytelecom.eu/catalog/5438.html) surveillance shop's [website](https://www.discoverytelecom.eu/catalog/5275.html), and enjoy the native *"[integration with trojan horse intrusion platforms](https://www.pic-six.com/products/p6-fi5)"*.

![](/assets/blog/20200728/imsi1.png)  
*Source: Discovery Telecom*

And, if you still had doubts the Orwellian dystopian future is upon us, check out how surveillance companies are now even conveniently [attaching IMSI catchers to flying drones](https://www.uasvision.com/2017/11/27/eca-group-unveils-imsi-catcher-module-for-uav-it180/).

![](/assets/blog/20200728/imsi2.jpg)  
*Source: UAS Vision*

As it typically goes with network security, encryption goes a long way here too. If your Internet traffic is encrypted, attackers won't be able to hijack it and network injections would likely fail. And while security researchers and engineers will keep playing Whac-a-Mole with the surveillance industry, you can start equipping your phone with a VPN, installing [HTTPS Everywhere](https://www.eff.org/https-everywhere) in your browser, and protect your websites with [Let's Encrypt](https://letsencrypt.org/).
