---
layout: default
title: Posts
---

## Posts

<p class="noindent">Sometimes I write posts too.</p>

<table class="table table-sm table-fit">
<tbody>
{% assign filtered-posts = site.posts | where: "categories", "Posts" %}
{%- for post in filtered-posts -%}
<tr>
  {%- assign date_format = site.minima.date_format | default: "%m/%d/%y" -%}
  <td><span class="post-meta">{{ post.date | date: date_format }}</span></td>
  <td>
    <a class="post-link" href="{{ post.url | relative_url }}">
      {{ post.title | escape }}
    </a>
    {% if post.tags != empty %}
        <span class="badge badge-warning text-wrap text-left">
            {{ post.tags | array_to_sentence_string: "" }}
        </span>
    {% endif %}
  </td>
</tr>
{%- endfor -%}
</tbody>
</table>

<p class="noindent">You can also find the old weekly readings <a href="{{ site.baseurl }}{% link weekly.md %}">here</a>.</p>