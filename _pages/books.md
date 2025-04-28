---
layout: page
title: Book Shelf
permalink: /books/
description: A collection of books that have transformed my approach to work and life.
nav: true
nav_order: 3
display_categories: [productivity, self-improvement, focus, happiness]
horizontal: false
---

<!-- pages/books.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized books -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_books = site.books | where: "category", category -%}
  {%- assign sorted_books = categorized_books | sort: "importance" %}
  <!-- Generate cards for each book -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for book in sorted_books -%}
      {% include books_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for book in sorted_books -%}
      {% include books.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display books without categories -->
  {%- assign sorted_books = site.books | sort: "importance" -%}
  <!-- Generate cards for each book -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for book in sorted_books -%}
      {% include books_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for book in sorted_books -%}
      {% include books.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
