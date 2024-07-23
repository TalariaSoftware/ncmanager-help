---
title: News
layout: home
---

# News

Updates about NCMS (the Neighborhood Council Management System) and things that
are interesting to people involved in neighborhood councils.

<ul class="usa-collection">
  {% for post in site.posts %}
    <li class="usa-collection__item">
      <div class="usa-collection__body">
        <h4 class="usa-collection__heading">
          <a class="usa-link" href="{{ post.url }}">
            {{ post.title }}
          </a>
        </h4>
        <p class="usa-collection__description">
          {{ post.excerpt }}
        </p>
        <ul class="usa-collection__meta" aria-label="More information">
          <li class="usa-collection__meta-item">
            <time datetime="{{ post.date | date_to_xmlschema }}">
              {{ post.date | date: "%B %e, %Y" }}
            </time>
          </li>
        </ul>
        <ul class="usa-collection__meta" aria-label="Topics">
          {% for tag in post.tags %}
            <li class="usa-collection__meta-item usa-tag">{{ tag }}</li>
          {% endfor %}
        </ul>
      </div>
    </li>
  {% endfor %}
</ul>
