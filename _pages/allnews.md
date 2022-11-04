---
title: "Machine Learning and Vision Group - News"
layout: textlay
excerpt: "Machine Learning and Vision Group News"
sitemap: false
permalink: /allnews.html
---

<h1 class='page-header'>
News
</h1>

{% for article in site.data.news %}
<p style="color: #777676"><span style="font-family: monaco, monospace; background-color: #f4733e38; color: #526069">({{ article.date }})</span>: {{ article.headline }}</p>
{% endfor %}
