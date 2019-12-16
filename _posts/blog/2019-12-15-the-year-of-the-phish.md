---
layout: post
title: The Year of the Phish
newsletter: True
categories: blog
---

Throughout 2019 we have seen phishing tactics evolve and mutate. We have seen a resurgence of [traditional forms](https://www.amnesty.org/en/latest/research/2019/03/phishing-attacks-using-third-party-applications-against-egyptian-civil-society-organizations/) as well as [new variations](https://www.amnesty.org/en/latest/research/2019/08/evolving-phishing-attacks-targeting-journalists-and-human-rights-defenders-from-the-middle-east-and-north-africa/) of OAuth Phishing; we have seen bypasses of two-factor authentication [becoming mainstream](https://www.amnesty.org/en/latest/research/2018/12/when-best-practice-is-not-good-enough/); and we have finally come across a campaign of targeted phishing attacks against human rights defenders using [reverse proxies](https://www.zdnet.com/article/new-tool-automates-phishing-attacks-that-bypass-2fa/) and session hijacking, which we will disclose in an upcoming report. As the end of the year approaches, security vendors release statistics and analyses from the data they have collected over 2019, with the likes of Google and Microsot also having seen phishing making a come back. A few days ago Microsoft's Office 365 Threat Research Team published a blog post titled [*"The quiet evolution of phishing"*](https://www.microsoft.com/security/blog/2019/12/11/the-quiet-evolution-of-phishing/), where they detail the more innovative techniques adopted by phishers in 2019. While the tricks Microsoft identified do not align with those we observed throughout Amnesty's work in the last year, we seem to arrive to some of the same conclusions:

> *"In 2019, we saw phishing attacks reach new levels of creativity and sophistication."*

Microsoft also launched an [interactive site](https://www.microsoft.com/securityinsights/) complementing their annual Security Intelligence Report, where you can visualize Redmond's visibility into attacks from the previous 12 months. I recommend taking a look. I enjoy analyzing these statistics to identify patterns and verify discrepancies or similarities to my own observations. According to their data, Microsoft saw a [decrease in malware encounters](https://www.microsoft.com/securityinsights/Malware) on Windows computers since 2018, which they attribute to the *"growth in adoption of Windows 10, and increased use of Windows Defender for protection"*.

![](/assets/blog/20191215/microsoft.png)

On the other hand, they document an ever [growing popularity of DDoS attacks](https://www.microsoft.com/securityinsights/DDoS), as well as an [increase in phishing email detections](https://www.microsoft.com/securityinsights/Phishing), which peaked at around 0.85% of all emails Microsoft analyzed in July 2019.

Similarly, according to telemetry from [Google Safe Browsing's Transparency Report](https://transparencyreport.google.com/safe-browsing/overview), malware sites have rapidly become a rare occurrence while phishing sites have skyrocketed.

![](/assets/blog/20191215/safebrowsing.png)

I do not know how to best interpret these graphs, but they seem indicative of a radical change occurring over the last two years. Browsers have certainly made leaps when it comes to security, and perhaps changes over the last couple of years have rendered malware delivery unfeasible. Phishing, instead, is either much more effectively detected or on a worrying rise. Are DDoS and phishing becoming the tactics of choice in response to a greater difficulty in infecting devices? Is malware becoming economically disadvantageous? Or simply the vectors have changed? I am interested to hear your take on what these statistics might tell us.

Because phishing is such a dominant threat for the targeted groups I normally work with, I have been working over the last years on a number of tools and services to mitigate and respond to such attacks. While I will hopefully share more details about some of those in the future, **I decided to release now a 25GB archive of data on the latest 100'000 phishing sites one of my systems processed.** This archive contains a SQLite database with a list of original URLs retrieved from various feeds, the final URL it eventually redirected to, as well as the DOM HTML and a screenshot of the page.

You can download it using this Torrent magnet link:

`magnet:?xt=urn:btih:28f02613928c2666f7a8f70be4079c1084012cbb&dn=phishing.zip&tr=udp%3A%2F%2Ftracker.openbittorrent.com%3A80`

If you are a security trainer looking for a large collection of phishing screenshots to use in educational material, or if you are an academic studying phishing, or a security analyst looking to test your organization's defenses, you might find this dataset useful. If you do, please let me know, as I am interested to learn of any derived insight or clever use.
