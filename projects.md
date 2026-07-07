---
layout: default
title: "Projects"
description: "Data products and studies Emmett Storts has built, from an attribution pipeline to a RAG search tool. Built in public."
permalink: /projects/
---

<section class="projects-index">
  <div class="container">
    <h1>Projects</h1>
    <p class="section-intro">Things I have built and am building. Each one is here as evidence of how I work, not as a product for sale. Live where it says live, in progress where it says in progress.</p>

    {% assign projects = site.projects | sort: "order" %}
    {% if projects.size > 0 %}
      <div class="project-grid">
        {% for project in projects %}{% include project-card.html project=project %}{% endfor %}
      </div>
    {% else %}
      <p>Projects are on the way.</p>
    {% endif %}
  </div>
</section>

{% include cta.html line="Want to talk through any of these, or the role you're hiring for? Book a call." location="projects-index-bottom" %}
