---
layout: default
title: Tags
---

{%-include back_link.html-%}

<h1>{{ page.title }}</h1>

{%- assign all_tags = site.posts | map: "tags" | flatten | uniq | sort -%}

<div class="tags-index">
  {%- for tag in all_tags -%}
    {%- assign slug = tag | slugify -%}
    <section class="tag-group" id="tag-{{ slug }}">
      <h2 class="tag-heading">{{ tag }}</h2>
      <ul class="post-list">
        {%- for post in site.posts -%}
          {%- if post.tags contains tag -%}
            <li>
              <span class="post-date">{{- post.date | date: site.theme_config.date_format -}}</span>
              <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
              {%- if post.description -%}
                <p class="post-description">{{ post.description }}</p>
              {%- endif -%}
            </li>
          {%- endif -%}
        {%- endfor -%}
      </ul>
    </section>
  {%- endfor -%}
</div>
