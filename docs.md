---
layout: page
title: Docs
permalink: /docs/
---



<ul class="post-list">
  {%- assign date_format = site.date_format | default: "%b %-d, %Y" -%}
  {%- for post in site.posts -%}
  <li>
    <h2>
      <a href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h2>
    <p class="post-meta">
      <time class="dt-published" datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">
        {{ post.date | date: date_format }}
      </time>
      {%- if jekyll.environment == "production" and site.disqus -%}
        • <a href="{{ post.url | relative_url }}#disqus_thread">
            <span class="disqus-comment-count" data-disqus-url="{{ post.url | absolute_url }}"></span>
          </a>
      {%- endif -%}
    </p>
    {%- if post.show_excerpts != false -%}
      <div class="post-excerpt">{{ post.excerpt | strip_html }}</div>
    {%- endif -%}
  </li>
  {%- endfor -%}
</ul>
