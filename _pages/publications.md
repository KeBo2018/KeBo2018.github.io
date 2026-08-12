---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<p style="color: #7a8288;">
Selected publications. A complete list is available on
<a href="https://scholar.google.com/citations?user=jA9GICIAAAAJ&hl=en&oi=ao">Google Scholar</a>.
<span style="font-size: 0.9em;">(* denotes equal contribution.)</span>
</p>

{% assign articles = site.publications | where: "category", "articles" | sort: "date" | reverse %}
{% assign chapters = site.publications | where: "category", "chapters" | sort: "date" | reverse %}
{% assign manuscripts = site.publications | where: "category", "manuscripts" | sort: "date" | reverse %}

<h2 style="margin-top: 1.5em;">Peer-reviewed journal articles</h2>

{% for post in articles %}
  <p style="padding-left: 2em; text-indent: -2em; margin-bottom: 1em; line-height: 1.6;">
    {{ post.citation }}{% if post.paperurl %} <a href="{{ post.paperurl }}">{{ post.paperurl }}</a>{% endif %}
  </p>
{% endfor %}

<h2 style="margin-top: 2em;">Book chapters</h2>

{% for post in chapters %}
  <p style="padding-left: 2em; text-indent: -2em; margin-bottom: 1em; line-height: 1.6;">
    {{ post.citation }}{% if post.paperurl %} <a href="{{ post.paperurl }}">{{ post.paperurl }}</a>{% endif %}
  </p>
{% endfor %}

<h2 style="margin-top: 2em;">Preprints and manuscripts under review</h2>

{% for post in manuscripts %}
  <p style="padding-left: 2em; text-indent: -2em; margin-bottom: 1em; line-height: 1.6;">
    {{ post.citation }}{% if post.paperurl %} <a href="{{ post.paperurl }}">{{ post.paperurl }}</a>{% endif %}
  </p>
{% endfor %}
