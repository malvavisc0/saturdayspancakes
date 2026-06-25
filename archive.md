---
layout: default
title: Archive
---

{%-include back_link.html-%}

<h1>{{ page.title }}</h1>

{%- assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" -%}

<div class="archive">
  {%- for year_group in posts_by_year -%}
    <section class="archive-year">
      <h2 class="archive-year-heading">{{ year_group.name }}</h2>
      <ul class="post-list">
        {%- for post in year_group.items -%}
          <li>
            <span class="post-date">{{- post.date | date: site.theme_config.date_format -}}</span>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            {%- if post.description -%}
              <p class="post-description">{{ post.description }}</p>
            {%- endif -%}
          </li>
        {%- endfor -%}
      </ul>
    </section>
  {%- endfor -%}
</div>
