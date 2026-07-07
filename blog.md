---
layout: default
title: "Writing"
description: "Writing on experimentation, causal inference, and building data products in public, by Emmett Storts."
permalink: /blog/
---

<section class="blog-index">
  <div class="container">
    <h1>Writing</h1>
    <p class="section-intro">Notes on experimentation, causal inference, and what it takes to build data products end to end. I work in public here, so expect reasoning and dead ends, not just finished results. <a href="{{ '/feed.xml' | relative_url }}">Subscribe by RSS.</a></p>

    {% if site.posts.size > 0 %}
      <ul class="post-list">
        {% for post in site.posts %}{% include post-card.html post=post %}{% endfor %}
      </ul>
    {% else %}
      <p>No posts yet.</p>
    {% endif %}
  </div>
</section>

{% include cta.html line="If a post makes you think we should talk, book a call." location="blog-index-bottom" %}
