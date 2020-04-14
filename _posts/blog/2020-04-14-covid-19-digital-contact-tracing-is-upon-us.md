---
layout: post
title: COVID-19 Digital Contact Tracing Is Upon Us
newsletter: True
categories: blog
---

Just like everybody else, I am also following the ongoing developments on digital contact tracing as an aid to contrast the COVID-19 pandemic. Perhaps to nobly oppose the initial calls for a dystopic panopticon by certain authorities, over the last few weeks universities, independent groups, and all sorts of private and public consortiums authored proposals for the development of contact tracing apps. Few days ago Google and Apple historically joined forces to seal the deal with a self-described ["Privacy-Preserving Contact Tracing"](https://www.apple.com/covid19/contacttracing/) framework, taking the upperhand and anticipating probable regulations.

Any digital contact tracing proposal, be it more or less respecting of privacy and human rights, demands high scrutiny. Are governments even taking basic public health and containment measures while advocating for more surveillance powers? Is digital contact tracing even necessary? Is it proportionate?

Some of these questions can't be answered yet, because we live in unprecedented circumstances in an unprecedented inter-connected world. There is no evidence to neither support nor dismiss the merit of digital contact tracing, and that puts us in an awkward spot. Navigating the conflict between allowing for additional forms of tracking and accepting a technology that might benefit public health is complicated. Having to decide quickly makes it all even more daunting.

And just like everybody else, I am also wondering about the societal impact, the inequity, the technological divide, the epidemiological science, and all the other dividing factors in this debate. We are Internet people, opinionated by design. Yet, despite strongly believing these factors to be of much higher importance than technical details, I am going to recuse myself from debating those issues here and concentrate on the geeky bits instead. (You can check Amnesty's [joint letter](https://www.amnesty.org/download/Documents/POL3020812020ENGLISH.pdf) addressing some of the big questions.)

While Bluetooth-based contact tracing was being proposed by [different](https://github.com/DP-3T/documents) [initiatives](https://www.covid-watch.org/) already, Apple's and Google's partnership comes as a stamp of approval of Silicon Valley and will perhaps close the debate around which underlying technology to use. Cellular towers data, Wi-Fi, GPS and similar alternatives are inadequate, and ACLU provides a good explainer for why [here](https://www.aclu.org/report/aclu-white-paper-limits-location-tracking-epidemic).

With Bluetooth, contact tracing apps would constantly emit and receive beacons (Bluetooth Low Energy broadcasts, to be precise) containing unique identifiers, and store records of all transmissions. When someone is diagnosed with COVID-19, all their identifiers emitted in the previous 14 days would be uploaded to a central server. Through the app, all other users would regularly download an up-to-date list from the central server, compare it to their local copies of received beacons, and therefore determine whether they would have been exposed to an infected person. It sounds like a simple and elegant system, and some strong cryptography could make it resistant to some forms of deanonymization, and could attempt to prevent linkability.

However, Bluetooth has its pitfalls too. Turns out it isn't trivial to digitally quantify our human contacts. Being a radio protocol, Bluetooth is subject to environmental factors which could improve, or most likely degrade its signal strength used to approximate the physical distance to nearby devices. If you are in a park, or in a high-density housing project, if you have thick walls, or a stuffed backpack, if you are separated by a window, the determined "exposure" will most likely be skewed by your surroundings.

I suspect a lot of experimentation would be required to calibrate this system correctly, and to verify its reliability under the more disparate conditions. Is this increased radio noise going to lead to unintended consequences? How reliable would it be in high-density areas?

Tight controls would most likely need to be established by the operators in order to prevent pranks, jamming, flooding, and isolate other forms of voluntary as well as involuntary interference.

Apple and Google's proposal lacks details on implementation and roll-out. As it stands, it seems their framework would be used as a foundation by national health authorities to build their own apps on. Who is then going to operate the central "diagnosis servers"? How? Are the apps going to be audited and approved by Apple and Google? How would access to local databases be protected? How easily could this data be forensically extracted and how could it be misused then?

There are many unanswered questions, and many more questions which we'll only formulate as software updates start to roll out and as apps are launched. In all likelihood, we can expect national health authorities to announce adoption plans soon, hopefully paired with strict verification protocols to avoid the propagation of false-positives and false-negatives, and with particular care for more marginalized communities.

The efficacy of digital contact tracing depends on wide adoption, which is more likely in the more privileged segments of wealthy economies. This is why, even if effective, these technologies can only be complementary to equitable public health initiatives and international collaboration. Access to modern smartphones can not be a discriminatory factor for access to proper healthcare.
