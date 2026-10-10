---
layout: archive
title: "Sitemap"
permalink: /sitemap/
sitemap: false
author_profile: true
---

{% include base_path %}

A list of all the posts and pages found on the site. For you robots out there, there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.

<h2>Pages</h2>
{% for post in site.pages %}
{% if post.title and post.sitemap != false %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

{% if site.posts.size > 0 %}
<h2>Posts</h2>
{% for post in site.posts %}
{% unless post.sitemap == false %}
{% include archive-single.html %}
{% endunless %}
{% endfor %}
{% endif %}

<h2><a href="{{ '/projects/' | relative_url }}">Projects</a></h2>
{% for post in site.projects reversed %}
{% unless post.sitemap == false %}
{% include archive-single.html %}
{% endunless %}
{% endfor %}

<h2><a href="{{ '/macro-notes/' | relative_url }}">Macro notes</a></h2>
{% for post in site.macro_notes reversed %}
{% unless post.sitemap == false %}
{% include archive-single.html %}
{% endunless %}
{% endfor %}
