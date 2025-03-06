---
layout: page
title: portfolio
permalink: /portfolio/
description: A growing collection of your cool posts.
nav: true
nav_order: 3
display_categories: [sample]
horizontal: false
---

<!-- pages/portfolio.md -->
<div class="posts">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized posts -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_posts = site.posts | where: "category", category %}
  {% assign sorted_posts = categorized_posts | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_posts %}
      {% include posts_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_posts %}
      {% include posts.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display posts without categories -->

{% assign sorted_posts = site.posts | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_posts %}
      {% include posts_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_posts %}
      {% include posts.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
