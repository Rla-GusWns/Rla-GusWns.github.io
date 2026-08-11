---
permalink: /
title: "Hyunjun Kim"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am an Integrated M.S./Ph.D. student in the Robotics and Intelligent System Engineering Lab ([RISE LAB](https://rise.skku.edu/)) at Sungkyunkwan University (SKKU), supervised by Prof. [Hyungpil Moon](https://scholar.google.com/citations?hl=ko&user=kBU7Os0AAAAJ).

I received my B.S. degree in the School of Robotics from Kwangwoon University in 2025. My research interests include Vision-Language-Action (VLA) models and vision-based object recognition.

## Publications

{% include base_path %}
{% if site.publication_category %}
{% for category in site.publication_category %}
{% assign title_shown = false %}
{% for post in site.publications reversed %}
{% if post.category != category[0] %}{% continue %}{% endif %}
{% unless title_shown %}<h3>{{ category[1].title }}</h3>{% assign title_shown = true %}{% endunless %}
{% include publication-compact.html %}
{% endfor %}
{% endfor %}
{% else %}
{% for post in site.publications reversed %}
{% include publication-compact.html %}
{% endfor %}
{% endif %}
