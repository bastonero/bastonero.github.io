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
* Ph.D in Physics, University of Bremen, 2026 (expected)
* M.S. in Physics, University of Turin, 2020
* B.S. in Physics, University of Turin, 2018

Work experience
======
* February-September 2026: PostDoc
  * University of Bremen
  * Supervisor: Prof. Dr. Nicola Marzari
  
Languages
======
* Italian (native)
* English (fluent)
* German (basic)

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Outreach
======
  <ul>{% for post in site.outreach reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
