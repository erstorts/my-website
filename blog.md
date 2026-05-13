---
layout: default
title: "Writing"
description: "Notes on data, decisions, and what actually moves the numbers at a Series A SaaS."
permalink: /blog/
---

<section class="blog-index">
  <div class="container">
    <h1>Writing</h1>
    <p class="blog-intro">Notes on data, decisions, and what actually moves the numbers at a Series A SaaS.</p>

    {% if site.posts.size > 0 %}
      <ul class="post-list">
        {% for post in site.posts %}
          <li class="post-list-item">
            <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
            <p class="post-list-meta"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time></p>
            {% if post.excerpt %}
              <p class="post-list-excerpt">{{ post.excerpt | strip_html | strip_newlines }}</p>
            {% endif %}
          </li>
        {% endfor %}
      </ul>
    {% else %}
      <p>No posts yet.</p>
    {% endif %}
  </div>
</section>

{% include cta.html line="Twenty minutes. Tell me what's broken. I'll tell you whether I can help." location="blog-index-bottom" %}
