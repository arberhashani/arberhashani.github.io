---
layout: page
title: Projects
permalink: /projects/
---

<div class="projects">
  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <h3>
          <a href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        <p>{{ post.excerpt }}</p>
      </li>
    {% endfor %}
  </ul>
</div>
