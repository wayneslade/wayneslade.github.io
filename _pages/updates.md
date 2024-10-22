---
title: "Slade Lab @ FAU HBOI - News"
layout: textlay
excerpt: "Slade Lab at Florida Atlantic University Harbor Branch"
sitemap: false
permalink: /updates.html
---

<h1>Research Updates</h1>

<ul class="list-unstyled">
    {% for article in site.data.news %}
        <li class="media">
            <div class="media-body">
            <h4 class="mt-0 mb-1">{{ article.headline }}</h4>
            <p><small>{{ article.date }}</small></p>
            {{ article.content }}
            </div>
        </li>
    {% endfor %}
</ul>
