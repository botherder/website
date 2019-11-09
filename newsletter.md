---
layout: page
title: Newsletter
permalink: /newsletter/
---

I curate a personal newsletter where you can expect various reflections on cyber security, privacy and surveillance. You can also expect links I have found interesting, as well as books that I'm reading or updates on art projects I am working on.

<div class="text-center" style="border:2px solid black;padding: 1em;font-size: 20px;margin-top: 2em;margin-bottom: 2em;">
    <b><span style="font-size: 24px;"><i class="far fa-newspaper"></i></span> Subscribe to the Newsletter <a href="https://newsletter.nex.sx/subscription/B1UbVz2JQ">here</a>.</b> Yes, you can also receive it PGP encrypted.
</div>

<i>If you subscribe, your email address is only stored on a server I run with an open source newsletter software called [Mailtrain](https://github.com/Mailtrain-org/mailtrain), and it is not shared with anyone. The emails I send do not track clicks, do not carry advertisement, or otherwise attempt to invade your privacy in any possible way. Additionally, I only write plain-text emails ([disable HTML view!](https://twitter.com/botherder/status/995966058371670016)).</i>

<h2 style="margin-top: 1.5em;">Archive</h2>

<p>Here you can find an archive of some of the previous newsletters. Please note that this archive is selective and is not updated timely. Do subscribe to receive my writings straight to your email.</p>

<table style="margin-top: 1em; margin-bottom: 1em;">
{% for post in site.categories.blog %}
{% if post.newsletter %}
<tr>
    <td>{{ post.date  | date: "%b %-d, %Y" }}</td>
    <td><span class="title-font" style="font-size: 22px;"><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></span></td>
</tr>
{% endif %}
{% endfor %}
</table>
