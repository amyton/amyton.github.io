---
layout: page
title: Blog
permalink: /blog/
---

<h1 class="page-title">{{ page.title }}</h1>

<div class="small-12 medium-11 medium-centered large-9 columns large-centered">

    <ul class="post-list no-bullet">
        {% for post in site.posts %}
        <li>
            <div class="post-meta">
                <span class="post-date">{{ post.date | date_to_string }}</span>
            </div>

            <h2 class="post-title"><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
            <p class="excerpt">{{ post.content | strip_html | truncatewords: 50 }}</p>
        </li>
        {% endfor %} 
    </ul>

    <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
</div>
