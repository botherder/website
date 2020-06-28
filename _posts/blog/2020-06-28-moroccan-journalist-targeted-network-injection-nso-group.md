---
layout: post
title: Moroccan Journalist Targeted with Network Injection Attacks Using NSO Group's Tools
newsletter: True
categories: blog
---

On June 22nd, Amnesty International published our Security Lab's discovery of attacks against Omar Radi, a prominent journalist and human rights defender from Morocco. After conducting a forensic analysis of Omar's iPhone, we found signs of targeted network injection attacks and infection with NSO Group's Pegasus spyware.

[https://www.amnesty.org/en/latest/research/2020/06/moroccan-journalist-targeted-with-network-injection-attacks-using-nso-groups-tools/](https://www.amnesty.org/en/latest/research/2020/06/moroccan-journalist-targeted-with-network-injection-attacks-using-nso-groups-tools/)

Omar is a courageous journalist who, because of this work, received harassment and intimidation. On December 26th 2019, Moroccan authorities arrested him because of a tweet he posted months before, criticizing the sentencing of protesters from the Hirak region of Morocco. He was released some days later, but eventually convicted to a 4 months suspended sentence.

Forensic traces we recovered from this phone reveal that Omar was targeted repeatedly from early 2019 at least until the end of January 2020. NSO Group's Pegasus spyware was installed on his phone not through a malicious link sent via typical SMS, but through injection attacks over his mobile network.

These attacks were coducted either with a rogue cell tower, which we know NSO Group sells as "Tactical Network Element", or by leveraging access to the mobile operator used by Omar. In either case, the system monitored the phone's Internet traffic and waited for any HTTP clear-text request in order to automatically inject a malicious redirect to an exploit server. In this way, attackers exploit vulnerabilities in the browser without often unconvincing social engineering messages.

<img src="https://aineupstrmediaprd.blob.core.windows.net/media/23858/mo2.png?width=374.88284910965325&height=500" style="width: 400px;" />  
*Photo Credit: Becky Peterson/Business Insider*

For example, we found one successful infection occurred while Omar was using his Twitter app and clicked on a legitimate link from his timeline. We were amazed to find Omar in one occasion was so suspicious of these redirects that he managed to snap a screenshot of one undergoing.

<img src="/assets/blog/20200628/phone.png" style="width: 250px" />

We have found network injections used before in Marocco along NSO Group's spyware. In a [previous report from October 2019](https://www.amnesty.org/en/latest/research/2019/10/Morocco-Human-Rights-Defenders-Targeted-with-NSO-Groups-Spyware/), we published similar findings on attacks against Maati Monjib, a well-known Moroccan human rights activist. Omar recalls one time a network injection occurred he was actually having lunch with Maati, and he pulled out his phone to find something he had read online pertaining to their conversation.

While network injection isn't a new technique, I believe we documented its first known use over 3G/4G, and implicated in the deployment of NSO Group's Pegasus. SMS messages carrying malicious links were too recognizable and allowed to trivially identify targets just by digging around for known domains. Network injections are much more insidious to both recognize on the moment as well as identify later on.

Unfortunately, two days after our publication [Omar Radi was convoked by the National Brigade of Judicial Police (BNPJ)](https://www.theguardian.com/world/2020/jun/24/moroccan-police-summon-journalist-days-after-israeli-spyware-allegations) and interrogated in connection to *"ongoing investigation in regard to his being a suspect of obtaining funds from foreign sources related to intelligence groups"*. On Friday Omar released a statement you can read in French on [his Twitter account](https://twitter.com/OmarRADI/status/1276567435311747073). We are following the evolving situation and are calling for a stop to his harassment.
