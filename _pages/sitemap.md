---
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

A list of all the pages found on the site. For you robots out there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.

<h2>Pages</h2>
{% for post in site.pages %}
  {% include archive-single.html %}
{% endfor %}

<h2>Files</h2>
<a href="http://www.antoinesoetewey.com/files/booklist.html" target="_blank">Books</a>