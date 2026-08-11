---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Integrated M.S./Ph.D. in Intelligence Robotics, Sungkyunkwan University, 2025 – present
* B.S. in School of Robotics, Kwangwoon University, 2025

Teaching experience
======
* Instructor, July 25 and 28, 2026 — AI & Robotics Practical Training for Vocational High School Students
* Instructor, January 6 – February 3, 2026 — Practice of Autonomous Driving with the CARLA Simulator, Suwon Lifelong Learning Center
* Instructor, July 29 – August 21, 2025 — Robot Calibration Practice Using a Laser Tracker

Publications
======
<ul>
{% for post in site.publications reversed %}
  <li>
    {% if post.paperurl %}{% assign pub_link = post.paperurl %}{% else %}{% assign pub_link = post.url | prepend: base_path %}{% endif %}
    <a href="{{ pub_link }}">{{ post.title }}</a><br />
    <span class="cv-citation">{{ post.citation }}</span>
  </li>
{% endfor %}
</ul>
