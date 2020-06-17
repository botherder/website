---
layout: post
title: COVID-19 Apps and New Forms of Surveillance
newsletter: True
categories: blog
---

Yesterday Amnesty International published the findings of a research project our Security Lab conducted over the last few weeks of COVID-19 contact tracing apps deployed in several countries between Europe and Middle-East and North Africa.

[https://www.amnesty.org/en/latest/news/2020/06/bahrain-kuwait-norway-contact-tracing-apps-danger-for-privacy/](https://www.amnesty.org/en/latest/news/2020/06/bahrain-kuwait-norway-contact-tracing-apps-danger-for-privacy/)

Among those we identified Kuwait's Shlonik, Bahrain's BeAware, and Norway's Smittestopp among the most problematic. These three apps were singled out because of their ability to live stream GPS coordinates of users' devices every few minutes. In the case of Kuwait and Norway, the apps also conduct Bluetooth proximity tracking and upload records of contacts between users.

On Monday, after a back and forth with the Norwegian government, and after the national Data Protection Authority sent a letter requesting clarifications, Smittestopp was temporarily put on pause and all data collected thus far was deleted.

Data from Bahrain's BeAware was also connected to a show on national television called "Are you at home?", where randomly selected users of the app were called over the phone live on air and those found to be at home could win prize money.

In May we already highlighted the case of Qatar's EHTERAZ app which, besides being able to automatically collect Bluetooth "contacts" and optionally enable GPS tracking as well, we found to suffer a major privacy and security flaw in the generation of QR codes scanned by police patrols and checkpoints to ensure users are respecting quarantine measures. Our team discovered that anyone with the sufficient technical know-how would have been capable to extract the QR code for all EHTERAZ users, and obtain the names, designated confinement location, health status, and more, tied to Qatari national ID numbers. This issue was exacerbated by the consistent format of these ID numbers, which makes them trivial to enumerate and probe in bulk. While Qatari authorities immediately took action to minimize the exposure, and eventually rolled out an update to the app, privacy concerns remain.

We found many flavors of contact tracing apps. While most follow a centralized architecture, some automatically upload data recorded by the apps, others only do so upon request of health authorities or voluntary symptom reporting by the users. Many, such as in the case of Kuwait, Bahrain, and Qatar, require national ID numbers upon registration, allowing authorities to directly connect records to specific individuals. Others, such as in the case of Norway, only require a valid phone number.

All in all, concerns over necessity and proportionality of the invasion of people's right to privacy can be found across the board. While the efficacy of these measures is still highly debated, privacy-preserving models are already available and should be explored first. However, many governments rushed to roll out apps seemingly without proper considerations for human rights. Some were even not provided with any privacy policy at all.

Amnesty is demanding governments to be transparent about their plans. COVID-19 contact tracing apps should remain voluntary, free from incentives and penalties. We are not only concerned about the potentially unnecessary invasive designs of some of these apps, but also of potential discriminatory practices that could stem from an inequitable access to healthcare if these apps become too central to government's response to the pandemic.

Personally, I worry the introduction of some of these apps, particularly in certain regions, might lead to a normalization of excessive tracking that surely will have some lasting effects.

If interested, you can find some technical notes from our analyses here:  
[https://github.com/amnestytech/covid19-apps](https://github.com/amnestytech/covid19-apps)

And a Twitter thread highlighting some of the most interesting discoveries we made:  
[https://twitter.com/botherder/status/1272782015386050562](https://twitter.com/botherder/status/1272782015386050562)
