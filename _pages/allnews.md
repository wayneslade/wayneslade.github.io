---
title: "Slade Lab @ FAU HBOI - News"
layout: textlay
excerpt: "Slade Lab at Florida Atlantic University Harbor Branch"
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br> {{ article.headline | markdownify}}</p>
{% endfor %}
