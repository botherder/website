---
layout: post
title: German-made FinSpy spyware found in Egypt, and Mac and Linux versions revealed
newsletter: True
categories: blog
---

Like in a return to old classics, last week my team and I published [a technical report](https://www.amnesty.org/en/latest/research/2020/09/german-made-finspy-spyware-found-in-egypt-and-mac-and-linux-versions-revealed/) detailing the discoveries of FinSpy in Egypt as well as of previously unknown variants for Mac OS and Linux. FinSpy is a suite of commercial-grade spyware produced by Munich-based FinFisher. I first published on FinFisher in 2012, when through early Internet scanning I had identified numerous FinSpy servers due to their odd "Hello Steffi" responses to my automated probes. And 8 years later, here we go again.

This time around we discovered samples of FinSpy in the hands of Egyptian state-sponsored group NilePhish, another familiar name to us and those of you reading this newsletter. While we found no indications on who they targeted, this discovery further implicates NilePhish as a likely state actor, considering FinSpy is self-admittedly only sold to law enforcement and intelligence agencies. FinFisher, in fact, first gained notoriety when protesters broke into the offices of Mubarak's secret police during the Egyptian revolution, and they found [contracts for the sale of FinSpy to the authorities](https://www.theguardian.com/technology/2011/apr/28/egypt-spying-software-gamma-finfisher).

While investigating this newly found FinSpy, we somewhat accidentally discovered an unrelated webserver which left exposed samples of FinSpy for Windows, Android as well as Mac OS and Linux, which were never previously reported on. As geeky as it sounds, stumbling into government spyware is a thrill, due to its supposed evasive and secretive nature, but this time around someone was evidently rather careless. We shared our discovery with the public and the research community because the opportunity to exhamine commercial spyware for Mac OS and Linux especially is rare. Quite obviouly these platforms are not immune from surveillance software, and if anything, a deeper analyis of these new variants shows that, especially on Linux, they work quite effortlessly.

Among the many modules it is provided with, FinSpy for Mac and Linux is capable of listing files, recording accessed modified, and deleted files, execute commands, log keystrokes, record the audio, the desktop and the webcam, intercept Skype calls and messages, scan for surrounding Wi-Fis, and steal emails from Thunderbird and Apple Mail.

Interestingly, a year ago, German media reported that [prosecutors in Munich have launched an investigation against the company](https://www.dw.com/en/german-prosecutors-investigate-spyware-maker-finfisher/a-50293812), following a complaint brought by some German NGOs suggesting some export improprieties might have occurred. Rather shockingly, a spokesperson from the Ministry of Economony stated to the press that the government did not issue any license for the export of spyware since the entry into force of stricter regulation in 2015. You've got to wonder what German surveillance vendors are doing and how effectively export controls are working in their current form.

[In a separate investigation](https://www.amnesty.org/en/latest/news/2020/09/eu-surveillance-sales-china-human-rights-abusers/) published a few days before, Amnesty also revealed how European companies routinely export other surveillance technologies, such as face recognition cameras, to China: *"Morpho, which is now part of Idemia, a French multinational, was awarded a contract to supply facial recognition equipment directly to the Shanghai Public Security Bureau in 2015. The company specializes in security and identity systems, including facial recognition systems and other biometric identification products. Amnesty International calls for a ban on the use, development, production, sale and export of facial recognition technology for identification purposes by both state agencies and private-sector actors."*

Many European governments are resisting calls to strengthen the current export controls regime, despite seemingly not working effectively enough. And for how much I regret speaking of the same issues I've been speaking of for the last decade, I regret more that it's because we haven't made much progress in curbing a snowballing surveillance industry. Perhaps it's time for [that moratorium](https://news.un.org/en/story/2019/06/1041231)?