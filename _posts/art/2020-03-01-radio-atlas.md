---
layout: artwork
title: "RADIO ATLAS"
info: 2020-
media: Digital installation
description: Installation analyzing smartphone radio emissions as unexplored space
permalink: art/radio-atlas/
categories: art
thumbnail: /assets/art/radio-atlas/radioatlas1.png
---
*~~A first version of RADIO ATLAS was exhibited at "[Practicing Sovereignty - Means of Digital Involvement](https://sovereignty.weizenbaum-institut.de/exhibitions/)" exhibition by [Weizenbaum Institute](https://www.weizenbaum-institut.de) in Berlin (Germany) from 12th to 18th March 2020.~~ (Unfortunately cancelled because of Coronavirus)*

{:.center}
<img src="/assets/art/radio-atlas/radioatlas1.png" style="box-shadow: none; margin-bottom: 0;" />

Our strive to regain control of our data begins with the understanding of where and how it travels. Radio Atlas is an installation composed of multiple computers probing radio frequencies typically occupied by Wi-Fi, Bluetooth and Mobile networks. Through these frequencies, smartphones, our most intimate and faithful possessions, are constantly announcing themselves and looking for familiar systems and networks without our knowledge. Because of this, these devices can easily be tracked, confessing patterns of our daily lives. Radio Atlas is an attempt to visualize, provide a cartography, of the surrounding radio entities: an observatory revealing an unexplored space that is invisible and unknown to most, and yet extremely crowded.

{:.center}
![](/assets/art/radio-atlas/radioatlas_photo.jpg)
*Photo by Berlin UDK*

RADIO ATLAS runs on three computers.

The first one uses Software Defined Radio to collect data broadcasted on frequencies used by mobile operators' cellular towers. Phones connect to these towers to access the Global System for Mobile Communication, more commonly known as the GSM network, in order to be able to instantiate phone calls and exchange SMS messages. GSM was introduced in the early 1990s, and in Europe it typically occupies the 900 MHz frequency band. Phones broadcast messages over these frequencies, some which contain unencrypted sensitive information. RADIO ATLAS identifies International Mobile Subscriber Identity (IMSI) numbers of devices in the vicinity. Your IMSI number is provisioned in the SIM card you use, and it identifies your phone in the cellular network. It can be used to track your phone, and potentially carry digital attacks against you. Since its launch GSM has not changed much, and due to its serious weaknesses it remains insecure. Many countries are planning to decommission it.

The second computer identifies surrounding devices emitting data over Wi-Fi or Bluetooth. Smartphones like to be connected to Wi-Fi, and they constantly broadcast the name of the network they are most familiar with, potentially leaking information about your own home networks. Wi-Fi typically uses 2.4 GHz or 5 GHz frequency bands. Similarly, smartphones constantly announce themselves over Bluetooth as well, offering to be connected to headphones, speakers and other accessories. Bluetooth operates over 2.4 GHz radio frequency bands. All these broadcasts can and have been used in the past to track movements of people, or for crowd control. RADIO ATLAS looks for Wi-Fi and Bluetooth-enabled devices too.

<iframe src="https://player.vimeo.com/video/488505156" width="640" height="440" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
<p><a href="https://vimeo.com/488505156">RADIO ATLAS</a> from <a href="https://vimeo.com/botherder">Nex</a> on <a href="https://vimeo.com">Vimeo</a>.</p>

All this harvested information is visualized live by a third computer, which plots the identified devices as stylized stars, comets, and novas. Conceptually, RADIO ATLAS is a *radio observatory* scanning through this *space* of electronic communications which remains oblivious to the typical consumers, confronting them with the amount of data constantly broadcasted by our smartphones.

All the information displayed is volatile. No data is stored.

*Built using Processing, Python 3, [bettercap](https://bettercap.org), [grgsm](https://github.com/ptrkrysik/gr-gsm).*
