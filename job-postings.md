---
layout: job-page
title: Career Development Job Postings
permalink: /job-postings/
---

<div class="home">

  <h1 class="page-heading">Job Postings</h1>

  <ul class="post-list">
    {% for post in site.posts %}
      {% if post.category == "job-listing" %}
        <li>
          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

          <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h2>
          {{ post.excerpt }}
        </li>
      {% endif %}
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
