---
layout: archive
title: "CV"
permalink: /cv-json/
author_profile: false
redirect_from:
  - /resume-json
---

{% include base_path %}

{% include cv-template.html %}

<div class="cv-download-links">
  {% if site.cv_pdf %}
  <a href="{{ base_path }}/files/{{ site.cv_pdf }}" class="btn btn--primary">Download CV as PDF</a>
  {% endif %}
  <a href="{{ base_path }}/cv/" class="btn btn--inverse">View Markdown CV</a>
</div>
