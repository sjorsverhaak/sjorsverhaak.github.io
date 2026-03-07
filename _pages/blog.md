---
layout: default
permalink: /blog/
title: Posts
nav: true
nav_order: 4
pagination:
  enabled: true
  collection: posts
  permalink: /page/:num/
  per_page: 5
  sort_field: date
  sort_reverse: true
  trail:
    before: 1
    after: 5
---

<style>
  /* Fade-in on load */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(14px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .posts-wrapper > * {
    opacity: 0;
    animation: fadeUp 0.6s ease forwards;
  }
  .posts-wrapper > *:nth-child(1) { animation-delay: 0.05s; }
  .posts-wrapper > *:nth-child(2) { animation-delay: 0.15s; }
  .posts-wrapper > *:nth-child(3) { animation-delay: 0.25s; }

  .post-list li {
    opacity: 0;
    animation: fadeUp 0.55s ease forwards;
  }
  .post-list li:nth-child(1) { animation-delay: 0.3s; }
  .post-list li:nth-child(2) { animation-delay: 0.4s; }
  .post-list li:nth-child(3) { animation-delay: 0.5s; }
  .post-list li:nth-child(4) { animation-delay: 0.6s; }
  .post-list li:nth-child(5) { animation-delay: 0.7s; }

  .posts-wrapper {
    font-family: 'EB Garamond', Georgia, serif;
    max-width: 780px;
  }
  .posts-header {
    margin-bottom: 2rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid #d0e8dc;
  }
  .posts-label {
    display: block;
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.78em;
    font-weight: 600;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #52b788;
    margin-bottom: 0.4em;
  }
  .posts-heading {
    font-family: 'Cormorant Garamond', Georgia, serif !important;
    font-size: 2.2rem;
    font-weight: 400;
    color: #1b4332;
    margin: 0;
  }
  .post-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  .post-list li {
    padding: 1.5rem 0;
    border-bottom: 1px solid #e8e4dc;
  }
  .post-list li:last-child {
    border-bottom: none;
  }
  .post-list h3 {
    margin: 0 0 0.3em 0;
  }
  .post-list h3 a.post-title {
    font-family: 'Cormorant Garamond', Georgia, serif !important;
    font-size: 1.45rem;
    font-weight: 400;
    color: #1b4332;
    text-decoration: none;
    border-bottom: none;
  }
  .post-list h3 a.post-title:hover {
    color: #2d6a4f;
    border-bottom: 1px solid #52b788;
  }
  .post-list p {
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 1.05em;
    color: #5a5a5a;
    margin: 0.3em 0;
    line-height: 1.6;
  }
  .post-meta, .post-tags {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.82em;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: #52b788;
    margin: 0.4em 0 0 0;
  }
  .post-meta a, .post-tags a {
    color: #52b788;
    text-decoration: none;
  }
  .post-meta a:hover, .post-tags a:hover {
    color: #2d6a4f;
  }
  /* Featured posts */
  .featured-posts .card {
    border: 1px solid #d0e8dc;
    border-radius: 3px;
    box-shadow: 0 2px 12px rgba(27,67,50,0.06);
  }
  .featured-posts .card-title {
    font-family: 'Cormorant Garamond', Georgia, serif !important;
    color: #1b4332;
    font-weight: 400;
  }
  .featured-posts .card-text {
    font-family: 'EB Garamond', Georgia, serif;
    color: #5a5a5a;
  }
</style>

<div class="posts-wrapper">

  {% assign blog_name_size = site.blog_name | size %}
  {% assign blog_description_size = site.blog_description | size %}

  {% if blog_name_size > 0 or blog_description_size > 0 %}
  <div class="posts-header">
    <h1 class="posts-heading">{{ site.blog_name }}</h1>
    {% if blog_description_size > 0 %}
      <p style="font-family: 'Cormorant Garamond', Georgia, serif; font-style: italic; color: #2d6a4f; margin: 0.5em 0 0 0; font-size: 1.1em;">{{ site.blog_description }}</p>
    {% endif %}
  </div>
  {% endif %}

  {% assign featured_posts = site.posts | where: "featured", "true" %}
  {% if featured_posts.size > 0 %}
  <div class="container featured-posts" style="margin-bottom: 2rem;">
    {% assign is_even = featured_posts.size | modulo: 2 %}
    <div class="row row-cols-{% if featured_posts.size <= 2 or is_even == 0 %}2{% else %}3{% endif %}">
      {% for post in featured_posts %}
      <div class="col mb-4">
        <a href="{{ post.url | relative_url }}" style="text-decoration: none;">
          <div class="card hoverable">
            <div class="card-body">
              <div class="float-right"><i class="fa-solid fa-thumbtack fa-xs" style="color: #52b788;"></i></div>
              <h3 class="card-title text-lowercase">{{ post.title }}</h3>
              <p class="card-text">{{ post.description }}</p>
              {% assign read_time = post.content | number_of_words | divided_by: 180 | plus: 1 %}
              {% assign year = post.date | date: "%Y" %}
              <p class="post-meta">
                {{ read_time }} min read &nbsp;·&nbsp;
                <a href="{{ year | prepend: '/blog/' | relative_url }}">{{ year }}</a>
              </p>
            </div>
          </div>
        </a>
      </div>
      {% endfor %}
    </div>
  </div>
  <hr style="border-color: #d0e8dc;">
  {% endif %}

  <ul class="post-list">
    {% if page.pagination.enabled %}
      {% assign postlist = paginator.posts %}
    {% else %}
      {% assign postlist = site.posts %}
    {% endif %}

    {% for post in postlist %}
      {% if post.redirect contains '://' %}{% continue %}{% endif %}
      {% assign read_time = post.content | number_of_words | divided_by: 180 | plus: 1 %}
      {% assign year = post.date | date: "%Y" %}
      {% assign tags = post.tags | join: "" %}
      {% assign categories = post.categories | join: "" %}

      <li>
        {% if post.thumbnail %}
        <div class="row">
          <div class="col-sm-9">
        {% endif %}

        <h3>
          {% if post.redirect == blank %}
            <a class="post-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          {% else %}
            <a class="post-title" href="{{ post.redirect | relative_url }}">{{ post.title }}</a>
          {% endif %}
        </h3>
        <p>{{ post.description }}</p>
        <p class="post-meta">
          {{ read_time }} min read &nbsp;·&nbsp; {{ post.date | date: '%B %d, %Y' }}
        </p>
        <p class="post-tags">
          <a href="{{ year | prepend: '/blog/' | relative_url }}"><i class="fa-solid fa-calendar fa-sm"></i> {{ year }}</a>
          {% if tags != "" %}
            &nbsp;·&nbsp;
            {% for tag in post.tags %}
              <a href="{{ tag | slugify | prepend: '/blog/tag/' | relative_url }}"><i class="fa-solid fa-hashtag fa-sm"></i> {{ tag }}</a>{% unless forloop.last %}&nbsp;{% endunless %}
            {% endfor %}
          {% endif %}
          {% if categories != "" %}
            &nbsp;·&nbsp;
            {% for category in post.categories %}
              <a href="{{ category | slugify | prepend: '/blog/category/' | relative_url }}"><i class="fa-solid fa-tag fa-sm"></i> {{ category }}</a>{% unless forloop.last %}&nbsp;{% endunless %}
            {% endfor %}
          {% endif %}
        </p>

        {% if post.thumbnail %}
          </div>
          <div class="col-sm-3">
            <img class="card-img" src="{{ post.thumbnail | relative_url }}" style="object-fit: cover; height: 90%;" alt="image">
          </div>
        </div>
        {% endif %}
      </li>
    {% endfor %}
  </ul>

  {% if page.pagination.enabled %}
    {% include pagination.liquid %}
  {% endif %}

</div>
