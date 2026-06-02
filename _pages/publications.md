---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% include base_path %}

{% assign featured_publications = site.publications | where: "featured", true | sort: "featured_order" %}
{% for post in featured_publications %}
  {% include archive-single.html %}
{% endfor %}

{% assign regular_publications = site.publications | sort: "date" | reverse %}
{% for post in regular_publications %}
  {% unless post.featured %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}
